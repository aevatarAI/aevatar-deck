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

## 1. 池子服务多账号上线并通过全员并发压测

<div class="slide-meta"><span class="owner-tag">@Kaihuei</span> · <strong>Pool Service</strong> · Due Friday 3/6</div>

本周五（2026-03-06）前完成池子服务多账号上线并通过全员并发压测。

- 多账号接入：≥ 5 个公司账号开通，均可正常登录并执行完整操作
- 全员并发压测：支持 ≥ 30 人并发请求，P99 响应时间 < 3s
- 输出压测报告与账号分配表

***

<div class="slide-section-label">交付物</div>

- 压测报告截图（含并发数、P99 响应时间）
- 账号分配表（含账号名、分配人、登录验证状态）

***

<div class="slide-section-label">验收标准</div>

- 压测 ≥ 30 并发，P99 < 3s
- ≥ 5 个账号开通且登录验证通过
- P0 阻塞 Bug = 0

***

<div class="slide-section-label">战略对齐</div>

- 团队研发效率提升：池子工具可用性直接影响全员日常开发人效
- 多账号 + 高并发保障是工具从"能用"到"好用"的关键卡点

---

## 2. Codex 安装配置 SOP 发布

<div class="slide-meta"><span class="owner-tag">@Kaihuei</span> · <strong>Codex</strong> · Due Friday 3/6</div>

本周五（2026-03-06）前完成 Codex 安装配置 SOP 发布，中国区 ≥ 7 位同事按文档独立完成安装。

- SOP 文档发布至团队知识库，链接可正常访问
- 中国区 ≥ 7 位同事按文档独立完成 Codex 安装
- 收集安装成功截图或文字确认

***

<div class="slide-section-label">交付物</div>

- SOP 文档链接（团队知识库）
- 同事安装成功截图/确认消息（含姓名，≥ 7 人）

***

<div class="slide-section-label">验收标准</div>

- SOP 链接可正常访问
- ≥ 7 位中国区同事确认独立完成安装
- 中国区 AI 工具渗透率从 0 → ≥ 50%

***

<div class="slide-section-label">战略对齐</div>

- AI 工具渗透率提升：Codex 安装成功率是 AI 辅助编码在团队落地的第一步
- 对齐"AI 工具覆盖率"KR

---

## 3. SoulGarden 核心监控告警上线

<div class="slide-meta"><span class="owner-tag">@Kaihuei</span> · <strong>SoulGarden</strong> · Due Friday 3/6</div>

本周五（2026-03-06）前完成 SoulGarden 核心监控告警在夜莺上线，Dashboard 展示 ≥ 4 项指标。

- 接入夜莺监控平台，配置 SoulGarden Dashboard
- Dashboard 展示 ≥ 4 项核心指标（CPU、内存、QPS、错误率）
- 配置 ≥ 1 条告警规则并通过触发测试

***

<div class="slide-section-label">交付物</div>

- Dashboard 访问链接
- 告警触发测试截图/通知记录

***

<div class="slide-section-label">验收标准</div>

- Dashboard 展示 ≥ 4 项核心指标
- ≥ 1 条告警规则触发测试通过
- 预期 MTTR 从 > 30min 降至 < 10min

***

<div class="slide-section-label">战略对齐</div>

- 服务稳定性增强：当前缺乏统一监控，故障发现依赖人工巡检
- 对齐"服务可用性 ≥ 99.9%"KR

---

## 4. Aefinder k8s 成本降低 ≥ 20%

<div class="slide-meta"><span class="owner-tag">@Kaihuei</span> · <strong>Aefinder</strong> · Due Friday 3/6</div>

本周五（2026-03-06）前完成 Aefinder k8s 月度服务器成本降低 ≥ 20%，服务可用性 ≥ 99.9%。

- 分析当前 k8s 资源使用，识别优化空间
- 执行资源缩减，确保降幅 ≥ 20%
- 验证缩减后全部服务健康检查通过

***

<div class="slide-section-label">交付物</div>

- 成本对比截图（云厂商账单页，标注优化前后金额）
- 服务健康状态截图

***

<div class="slide-section-label">验收标准</div>

- 优化前 vs 优化后月费降幅 ≥ 20%
- 缩减后连续 24h 无 P0/P1 告警
- 全部服务健康检查通过

***

<div class="slide-section-label">战略对齐</div>

- 基础设施成本降低：Aefinder k8s 月度费用直接影响毛利
- 对齐"基础设施成本优化"KR

---

## 5. Aetherlink 节点上线

<div class="slide-meta"><span class="owner-tag">@Kaihuei</span> · <strong>Aetherlink</strong> · Due Friday 3/6</div>

本周五（2026-03-06）前完成 Aetherlink 节点上线，区块同步至最新高度且健康检查通过。

- 部署 Aetherlink 节点上线
- 区块同步至最新高度，延迟 < 10 个区块
- 健康检查接口返回 200，连续 ≥ 1 小时无异常

***

<div class="slide-section-label">交付物</div>

- 节点状态截图（含区块高度）
- 健康检查日志（含连续 1h 时间戳）

***

<div class="slide-section-label">验收标准</div>

- 区块同步延迟 < 10 个区块
- 健康检查返回 200，连续 ≥ 1h 无异常
- 节点可用性满足业务上线要求

***

<div class="slide-section-label">战略对齐</div>

- 基础设施可用性：Aetherlink 节点是业务上线的前置依赖
- 对齐"Aetherlink Q1 上线"里程碑
