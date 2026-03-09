---
layout: deck
title: "Week 11 Plan"
date: 2026-03-09
week: "2026-W11"
type: plan
member: Kaihuei
---

## Week 11 Plan

**Aevatar Team** · March 9, 2026

---

## 1. SoulGarden 探针配置与 HPA 水平扩容上线

<div class="slide-meta"><span class="owner-tag">@Kaihuei</span> · <strong>Developer Platform / SoulGarden</strong> · Due Tuesday 3/10</div>

本周二（2026-03-10）前为 Developer Platform 上线探针配置和 HPA 水平扩容能力，将 SoulGarden 服务故障自愈时间从当前人工介入 30 分钟缩短至 K8s 自动重启 < 30 秒，并在流量突增时自动扩容以维持 P99 < 3s。

- 配置 liveness 探针：容器异常时 K8s 自动重启，故障自愈时间 < 30 秒
- 配置 readiness 探针：滚动更新零中断，仅健康 Pod 接收流量
- 配置 HPA：min 1 / max 10 / CPU 阈值 60%，流量突增时自动扩容
- 生产环境部署并验证探针与 HPA 生效
