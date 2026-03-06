---
layout: deck
title: "Week 10 Review"
date: 2026-03-06
week: "2026-W10"
type: review
member: louis
---

## Week 10 Review

**Aevatar Team** · March 6, 2026

---

## 1. 端到端链路追踪与 Jaeger 集成

<div class="slide-meta"><span class="owner-tag">@louis</span> · <strong>Aevatar</strong></div>

- 完成 stream-first tracing 端到端实现，集成 Jaeger 可视化
- 统一 trace_id、correlation_id、causation_id 三键协议，打通运行时日志与工作流 API 的追踪关联
- 对齐 HTTP/WebSocket/API 的追踪可见性，统一可观测性结构

***

### Jaeger 追踪可视化

<div style="position: relative; display: inline-block;">
<img src="{{ '/assets/images/week10-review-louis-jaeger-trace.png' | relative_url }}" alt="Jaeger Trace" style="max-height: 60vh;">
<div style="position: absolute; bottom: 8px; left: 8px; border: 2px solid #00f0ff; border-radius: 6px; padding: 2px 8px; background: rgba(0,240,255,0.15); color: #00f0ff; font-size: 0.7em; font-weight: 700; box-shadow: 0 0 12px rgba(0,240,255,0.4);">POST /chat · ~39.4s</div>
</div>

**性能洞察：**
- 完整工作流执行链路可见性：从 API 请求到事件完成的端到端追踪

***

### 日志中的追踪上下文传播

<div style="display: flex; justify-content: center; align-items: flex-start; height: 50vh;">
<img src="{{ '/assets/images/week10-review-louis-tracing-logs.png' | relative_url }}" alt="Tracing Logs" style="max-height: 45vh;">
</div>

**日志关联验证：**
- TraceId 在 ASP.NET Core 诊断层和 Aevatar 事件溯源层一致传播
- 同一 TraceId 跨不同日志类别可见，确保请求链路完整追踪
---

## 2. Metrics 可观测性基线建设

<div class="slide-meta"><span class="owner-tag">@louis</span> · <strong>Aevatar</strong></div>

- 统一 API 和运行时 metrics 接入方式，使用OTLP collector 架构，统一遥测数据导出
- 建立 Prometheus 告警规则（错误率、延迟 SLO 违规）
- Grafana 监控面板配置

***

### Runtime 概览面板

<div style="display: flex; justify-content: center; align-items: flex-start; height: 60vh;">
<img src="{{ '/assets/images/week10-review-louis-runtime-overview.png' | relative_url }}" alt="Runtime Overview Dashboard" style="max-height: 55vh;">
</div>

**SLO 指标（近 15 分钟）：**
- **错误率**：API 和运行时事件错误率均为 **0%**（健康）
- **首响应延迟 p95**：基线稳定，峰值 150-200ms
- **完整请求延迟 p95**：峰值 15-20s（反映 AI 生成时间波动）
- **运行时事件处理延迟**：稳定在 **~4.8ms**（p95/p99）

***

### Runtime 诊断面板

<div style="display: flex; justify-content: center; align-items: flex-start; height: 60vh;">
<img src="{{ '/assets/images/week10-review-louis-runtime-diagnostics.png' | relative_url }}" alt="Runtime Diagnostics Dashboard" style="max-height: 55vh;">
</div>

**诊断洞察（SLO 降级视图）：**
- **活跃 Actor**：**10 个实例**运行中
- **运行时自事件**：窗口内 **926 个事件**
- **API 请求**：窗口内 **3 个请求**
- **事件/请求比**：**308 事件/API 请求**
- **事件速率关联**：运行时事件与 API 请求

---
