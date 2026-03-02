---
layout: deck
title: "Week 10 Plan"
date: 2026-03-02
week: "2026-W10"
type: plan
member: Kaihuei
---

## Week 10 Plan

**Aevatar Team** · March 2, 2026

---

## 1. 池子服务多账号上线并完成压测

<div class="slide-meta"><span class="owner-tag">@Kaihuei</span> · <strong>Pool Service</strong> · Due Friday 3/6</div>

本周五（2026-03-06）前完成池子服务多账号上线并通过全员并发压测。

- 多账号接入：≥ 5 个公司账号开通，均可正常登录并执行完整操作
- 全员并发压测：支持 ≥ 30 人并发请求，P99 响应时间 < 3s
- 输出压测报告与账号分配表

---

## 2. Codex 安装配置 SOP 发布

<div class="slide-meta"><span class="owner-tag">@Kaihuei</span> · <strong>Codex</strong> · Due Friday 3/6</div>

本周五（2026-03-06）前完成 Codex 安装配置 SOP 发布，中国区 ≥ 7 位同事按文档独立完成安装。

- SOP 文档发布至团队知识库，链接可正常访问
- 中国区 ≥ 7 位同事按文档独立完成 Codex 安装
- 收集安装成功截图或文字确认

---

## 3. SoulGarden 核心监控告警上线

<div class="slide-meta"><span class="owner-tag">@Kaihuei</span> · <strong>SoulGarden</strong> · Due Friday 3/6</div>

本周五（2026-03-06）前完成 SoulGarden 核心监控告警在夜莺上线，Dashboard 展示 ≥ 4 项指标。

- 接入夜莺监控平台，配置 SoulGarden Dashboard
- Dashboard 展示 ≥ 4 项核心指标（CPU、内存、QPS、错误率）
- 配置 ≥ 3 条告警规则并通过触发测试

---

## 4. Aefinder k8s 成本降低 ≥ 20%

<div class="slide-meta"><span class="owner-tag">@Kaihuei</span> · <strong>Aefinder</strong> · Due Friday 3/6</div>

本周五（2026-03-06）前完成 Aefinder k8s 月度服务器成本降低 ≥ 20%，服务可用性 ≥ 99.9%。

- 分析当前 k8s 资源使用，识别优化空间
- 执行资源缩减，确保降幅 ≥ 20%
- 验证缩减后全部服务健康检查通过

---

## 5. Aetherlink Oracle 节点搭建与上线

<div class="slide-meta"><span class="owner-tag">@Kaihuei</span> · <strong>Aetherlink</strong> · Due Friday 3/6</div>

本周五（2026-03-06）前完成 Aetherlink 节点上线，区块同步至最新高度且健康检查通过。

- 部署 Aetherlink 节点上线
- 区块同步至最新高度，延迟 < 10 个区块
- 健康检查接口返回 200，连续 ≥ 1 小时无异常
