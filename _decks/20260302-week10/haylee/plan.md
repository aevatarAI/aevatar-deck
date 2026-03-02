---
layout: deck
title: "Week 10 Plan"
date: 2026-03-02
week: "2026-W10"
type: plan
member: Haylee
role: QA
---

## 项目 1：Sisyphus（Aevatar research）

测试地址：[https://sisyphus-test.aevatar.ai/](https://sisyphus-test.aevatar.ai/)

**目标与时限**：完成 3300 页论文全链路测试（解析 -> 入库 -> 图谱扩张 -> 24h 无人值守运行）。  
**验收标准**：
- 单篇一次跑通且无 P0/P1 阻断
- 3300 页任务 24h 连续运行，重启 = 0
- 抽检 20 节点，正确可读 >= 16
**交付物**：`Sisyphus` 测试报告 + Trace 截图证据包 + 最终证据链接  
**业务指标**：SLA 中断率、人工盯跑成本

---

## 项目 2：NyxID

测试地址：[https://nyx.chrono-ai.fun/](https://nyx.chrono-ai.fun/)

**目标与时限**：完成鉴权、连接与保障机制测试。  
**验收标准**：
- 成功率 >= 99%，401/timeout 占比 <= 1%
- 异常恢复 <= 10 分钟，超限 1 分钟内自动止损
- 日志检索 <= 3 分钟，回滚恢复 <= 15 分钟
**交付物**：`NyxID` 专项报告 + 止损/回滚验证记录 + 最终证据链接  
**业务指标**：平台可用率、故障恢复时长、运维排障成本
