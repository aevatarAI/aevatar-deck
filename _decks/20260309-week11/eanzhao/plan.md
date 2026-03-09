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

<div class="slide-meta"><span class="weight-badge">30%</span> <span class="owner-tag">@Eanzhao</span> · <strong>Execution Runtime</strong> · Due Friday 3/13 18:00</div>

在 Aevatar 内补齐浏览器自动化执行层，把“智能编排”和“页面执行”彻底解耦，支撑必须通过 Playwright 才能完成的浏览器搜索、下单等操作。

- Workflow / GAgent 负责理解意图、调用外部能力、处理失败重试、做人审、写入用户偏好记忆
- Playwright Bridge 负责把 Aevatar 的调用翻译成浏览器任务与会话上下文
- Playwright Worker 负责真实浏览器执行（页面选择器、截图、DOM 提取、点击/输入）

***

<div class="slide-section-label">新增 Workflow 原语（Playwright 必需）</div>

- `create_session`
- `navigate`
- `click`
- `fill`
- `wait_for`
- `snapshot`
- `extract_text`
- `screenshot`
- `close_session`

***

<div class="slide-section-label">交付物</div>

- `aevatar-playwright-architecture.md`（分层职责、调用时序、失败回传）
- `playwright-bridge-spec.md`（Aevatar 调用到 Worker 任务的翻译协议）
- Workflow 原语定义与示例 YAML（可直接编排）

***

<div class="slide-section-label">验收标准</div>

- 9 个通用原语在 staging 可独立调用并返回结构化结果
- 同一会话可跨多步复用上下文，`create_session` 到 `close_session` 生命周期完整
- Worker 失败能被 Bridge 标准化回传并被 Workflow 正确重试或转人工

---

## 2. 单用户偏好记忆 GAgent + 自动点餐 Workflow

<div class="slide-meta"><span class="weight-badge">30%</span> <span class="owner-tag">@Eanzhao</span> · <strong>Workflow Orchestration</strong> · Due Friday 3/13 18:00</div>

在 Twilio -> Grab 主链路中接入意图理解、补问、人审、重试和偏好写回，形成“能下单、可纠错、会记忆”的可用版本。

- 接收 Twilio 消息后解析订单意图，缺失字段自动补问，关键步骤支持人工确认
- 下单前注入单用户偏好（`channel + user_id` 维度），下单后回写偏好更新
- 对失败节点执行重试策略（限次重试 + 转人工兜底），避免流程中断

***

<div class="slide-section-label">交付物</div>

- `twilio-grab-order.yaml`（编排版本，接入 Playwright 原语）
- `user-preference-gagent.md`（记忆模型、更新规则、冲突覆盖/重置）
- Workflow 节点实现（intent-parser / slot-filler / human-review / preference-writer）

---

## 3. Grab 领域原语适配（暂定）

<div class="slide-meta"><span class="weight-badge">20%</span> <span class="owner-tag">@Eanzhao</span> · <strong>Grab Domain Primitives</strong> · Due Friday 3/13 18:00</div>

基于通用 Playwright 原语抽象 Grab 业务原语，沉淀可复用的“找店 -> 加购 -> 结算 -> 提交”能力块，降低 workflow 编排复杂度。

***

<div class="slide-section-label">Grab 原语（暂定）</div>

- `grab.search_merchant`
- `grab.open_merchant`
- `grab.add_item`
- `grab.set_note`
- `grab.open_cart`
- `grab.checkout_preview`
- `grab.submit_order`

***

<div class="slide-section-label">交付物</div>

- `grab-primitives-spec.md`（原语语义、输入输出、失败码）
- Grab 页面选择器与回退策略配置
- 原语级脚本样例（串联为可执行下单流程）

***

<div class="slide-section-label">验收标准</div>

- 7 个 Grab 原语可单测通过并可串联执行
- 页面结构轻微变化时具备回退 selector，核心链路不中断
- `grab.submit_order` 前默认经过 `grab.checkout_preview` 做最终人审校验
