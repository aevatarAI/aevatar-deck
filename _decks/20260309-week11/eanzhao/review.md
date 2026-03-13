---
layout: deck
title: "Week 11 Review"
date: 2026-03-13
week: "2026-W11"
type: review
member: Eanzhao
---

## Week 11 Review

**Aevatar Team** · March 13, 2026

---

## 1. Workflow 运行态与命令完成态

<div class="slide-meta"><span class="owner-tag">@Eanzhao</span> · <strong>Workflow</strong></div>

- 修复运行态状态管理不稳：`delay`、`wait-signal`、LLM call、secure input 等模块的状态承载方式调整，减少对脆弱运行时临时存储的依赖，移除过时 runtime store
- 修复命令投递到完成态语义不清：补强 detached dispatch、durable completion、live observation detachment 与 fallback，缩小「命令已接受但完成态不可确认」的灰区
- 整体收敛到更稳定的 `actor/state/protobuf/observation` 主干

---

## 2. Projection 与 Actor 绑定

<div class="slide-meta"><span class="owner-tag">@Eanzhao</span> · <strong>Projection / Actor</strong></div>

- Projection：新增自定义失败 payload，增强 activation/release、ownership 与错误处理分支，降低投影异常时的信息丢失与补偿难度
- Actor 绑定与读取：补上 `QueryActorAsync`，强化 binding reader、query client、actor port 校验，使 run actor 解析与读路径更明确
- Projection 编解码：对 legacy payload、session event transport、workflow run event codec 做统一与兼容，减少旧数据或跨版本消息导致的投影异常

---

## 3. 兼容性、事件路由与桥接

<div class="slide-meta"><span class="owner-tag">@Eanzhao</span> · <strong>Foundation / AI / Bridge</strong></div>

- 兼容与校验：legacy YAML 兼容、inline workflow 序列化改进、workflow name / run ID 校验，减少非法请求与历史载荷导致的执行失败
- 事件路由：envelope metadata、correlation、propagation、event routing 收敛到统一语义，进一步转向 `TopologyAudience`，减少多套路由并存歧义
- AI 会话与回放：RoleGAgent、ChatRuntime、ToolCallLoop、metadata 与 replay contract 补强，会话恢复、工具调用与事件回放更稳定
- Telegram bridge：清理旧 bridge/core/api 实现，改为 delegation，收口桥接逻辑

---

## 4. 总结

<div class="slide-meta"><span class="owner-tag">@Eanzhao</span> · <strong>Review</strong></div>

- 本周集中修复 **Workflow + Projection + Event Routing** 主干上的一组系统性问题，而非零散修 bug
- 影响范围：workflow（Application / Core / Infrastructure / Projection / Host API）、foundation/runtime、AI、bridge/cli
- 核心成果：状态边界更清晰、完成态更可观察、兼容性更好、事件语义更统一、桥接实现更收敛
