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

## 1. 统一 Metrics 接入方式与核心指标建设

<div class="slide-meta"><span class="owner-tag">@louis</span> · <strong>Aevatar</strong> · Due Friday 3/6</div>

本周五（2026-03-06）前完成统一 metrics 接入方式，增加核心 metrics 指标。

- 统一各服务的 metrics 接入方式与采集规范
- 定义并接入核心 metrics 指标（如 QPS、延迟、错误率、队列 depth 等）
- 建立最小观测面板，覆盖关键链路与关键错误视图

***

<div class="slide-section-label">交付物</div>

- 设计文档（统一接入规范、核心指标定义、采集方案）
- 对应改造 PR 链接
- 最小观测面板访问链接（链路视图 + 关键错误视图）

***

<div class="slide-section-label">验收标准</div>

- 设计文档通过 review 并落地
- 改造 PR merged，各关键服务接入统一 metrics
- 最小观测面板可访问，展示链路与关键错误视图
- 提升 aevatar 项目 Observability 能力，增强系统稳定性

***

<div class="slide-section-label">战略对齐</div>

- 提升 Observability 能力，建立统一可观测基线
- 增强系统稳定性，缩短问题发现与定位时间
- 为后续告警、SLO/SLI 建设打下基础

---

## 2. 链路追踪在关键链路的落地

<div class="slide-meta"><span class="owner-tag">@louis</span> · <strong>Aevatar</strong> · Due Friday 3/6</div>

本周五（2026-03-06）前完成链路追踪在关键链路的落地，保证完成跨节点上下文透传验证。

- 在关键链路中埋点并透传 trace_id
- 完成跨节点、跨服务上下文透传验证
- 打通日志与 Trace 关联，支持从问题发现到根因定位的端到端追踪

***

<div class="slide-section-label">交付物</div>

- 设计文档（三元组规范、埋点方案、透传协议）
- 改造 PR 链接
- 端到端日志 / Trace 截图（含三元组透传验证）

***

<div class="slide-section-label">验收标准</div>

- 设计文档通过 review，改造 PR merged
- 关键链路中 trace_id  可端到端透传
- 5 分钟以内完成从发现问题到定位问题（含日志/Trace 截图验证）
- 提升 aevatar Traceability 能力，快速定位问题，增强系统稳定性

***

<div class="slide-section-label">战略对齐</div>

- 提升 Traceability 能力，缩短故障定位时间
- 增强系统稳定性，降低 MTTR
- 支撑分布式系统的可观测与可调试能力
