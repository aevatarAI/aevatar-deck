---
layout: deck
title: "Week 10 Plan"
date: 2026-03-02
week: "2026-W10"
type: plan
member: louis
---

## Week 10 Plan

**Aevatar Team** · March 2, 2026

---

## 1. 可观测性与链路追踪建设

<div class="slide-meta"><span class="owner-tag">@louis</span> · <strong>Aevatar</strong> · Due Friday 3/6</div>

本周五（2026-03-06）前完成 metrics 统一接入、核心指标建设与 trace_id 在关键链路的落地。

- **Metrics**：统一各服务接入方式，定义核心指标（QPS、延迟、错误率等），建立最小观测面板（链路视图 + 关键错误视图）
- **Trace**：在关键链路埋点并透传 trace_id，完成跨节点上下文透传，打通日志与 Trace 关联

***

<div class="slide-section-label">交付物</div>

- 设计文档（Metrics 规范 + Trace 透传协议）+ 改造 PR 链接
- 最小观测面板访问链接 + 端到端日志/Trace 截图

***

<div class="slide-section-label">验收标准</div>

- 设计文档 review 通过，改造 PR merged
- 最小观测面板可访问；trace_id 关键链路端到端透传
- 5 分钟内从发现问题到定位问题

***

<div class="slide-section-label">战略对齐</div>

- 建立统一可观测基线，缩短故障发现与定位时间，降低 MTTR
- 提升 Observability / Traceability 能力，增强系统稳定性
