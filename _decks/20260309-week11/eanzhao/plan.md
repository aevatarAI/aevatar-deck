---
layout: deck
title: "Week 11 Plan"
date: 2026-03-09
week: "2026-W11"
type: plan
member: Eanzhao
---

## Week 11 Plan

**Aevatar Team** · March 9, 2026

---

## 1. Aevatar + Playwright 执行层（Bridge / Worker）

<div class="slide-meta"><span class="weight-badge">35%</span> <span class="owner-tag">@Eanzhao</span> · <strong>Execution Runtime</strong> · Due Friday 3/13 18:00</div>

在 Aevatar 内补齐 Playwright GAgent / Worker 执行层，把“智能编排”和“页面执行”彻底解耦，支撑点餐场景的稳定编排。

- Workflow / GAgent 负责理解意图、调用外部能力、处理失败重试、做人审、写入用户偏好记忆
- Playwright Bridge 负责把 Aevatar 的调用翻译成浏览器任务与会话上下文
- Playwright Worker 负责真实浏览器执行（页面选择器、截图、DOM 提取、点击/输入）

***

<div class="slide-section-label">新增 Workflow 原语（Playwright Call）</div>

- `playwright_call`
- `operation` values: `create_session` / `navigate` / `click` / `fill` / `wait_for` / `snapshot` / `extract_text` / `screenshot` / `close_session`

***

<div class="slide-section-label">编排方式（Workflow Call）</div>

- 使用 `playwright_call` 及其 `operation` values 组合 Playwright 子流程，并沉淀为可复用子 workflow
- Grab 点餐流程独立保存为 `grab-order-workflow.yaml`
- 主流程 `grab-main-workflow.yaml` 通过 `workflow_call` 调用子流程并接收结构化结果

***

<div class="slide-section-label">交付物</div>

- `playwright-bridge-spec.md`（Aevatar 调用到 Worker 任务的翻译协议）
- `playwright_call` 原语定义与示例 YAML（可直接编排）

***

<div class="slide-section-label">验收标准</div>

- Playwright GAgent 能稳定接收 `playwright_call` 请求并返回结构化结果
- `playwright_call` 在 staging 可稳定执行 9 个 `operation` values 并返回结构化结果
- 同一会话可跨多步复用上下文，`create_session` 到 `close_session` 生命周期完整
- Worker 失败能被 Bridge 标准化回传并被 Workflow 正确重试或转人工

---

## 2. 单用户偏好记忆 GAgent + 自动点餐 Workflow

<div class="slide-meta"><span class="weight-badge">35%</span> <span class="owner-tag">@Eanzhao</span> · <strong>Workflow Orchestration</strong> · Due Friday 3/13 18:00</div>

在 Grab 点餐主链路中，由主 workflow / GAgent 处理意图理解、补问、人审、重试和偏好写回，形成“能下单、可纠错、会记忆”的可用版本。

- 主 workflow 负责点餐意图理解，对缺失字段自动补问，关键步骤支持人工确认
- 主 workflow 通过 `workflow_call` 调用 `grab-order-workflow.yaml` 执行页面自动化子流程
- 下单前注入单用户偏好（`user_id` 维度），下单后回写偏好更新
- 对失败节点执行重试策略（限次重试 + 转人工兜底），避免流程中断

***

<div class="slide-section-label">交付物</div>

- `grab-main-workflow.yaml`（主流程：意图理解、补问、人审、偏好读写、`workflow_call`）
- `user-preference-gagent.md`（记忆模型、更新规则、冲突覆盖/重置）
- Workflow 节点实现（intent-parser / slot-filler / human-review / preference-writer）

***

<div class="slide-section-label">验收标准</div>

- 主流程可通过 `workflow_call` 成功触发 `grab-order-workflow.yaml` 并回收执行结果
- 在 staging 跑通 15 组脚本化场景，成功率 >= 90%
- 同一用户连续 20 轮对话偏好召回准确率 >= 85%
- 用户显式修改偏好后，下一次下单能正确应用新偏好且不与其他用户串扰

---

## 3. Grab 点餐子 Workflow（基于 `playwright_call`）

<div class="slide-meta"><span class="weight-badge">30%</span> <span class="owner-tag">@Eanzhao</span> · <strong>Grab Ordering Workflow</strong> · Due Friday 3/13 18:00</div>

不额外引入 `grab.*` 原语，而是直接使用 `playwright_call` 的不同 `operation` values 编排 Grab 点餐子 workflow，沉淀为可复用的独立 YAML，并由主 workflow 通过 `workflow_call` 调用。

***

<div class="slide-section-label">Grab 子流程关键步骤</div>

- 搜索商家
- 打开商家页
- 加购商品
- 填写备注
- 打开购物车
- 结算预览
- 提交订单

***

<div class="slide-section-label">交付物</div>

- `grab-order-workflow.yaml`（基于 `playwright_call` 的 Grab 点餐子流程）
- Grab 页面选择器与回退策略配置
- 子流程输入输出样例（供 `workflow_call` 复用）

***

<div class="slide-section-label">验收标准</div>

- `grab-order-workflow.yaml` 可由主 workflow 通过 `workflow_call` 调起并稳定完成主链路
- 页面结构轻微变化时具备回退 selector，核心链路不中断
- 提交订单前默认经过 checkout preview 与最终人审校验
