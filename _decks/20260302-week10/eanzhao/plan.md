---
layout: deck
title: "Week 10 Plan"
date: 2026-03-02
week: "2026-W10"
type: plan
member: Eanzhao
---

## Week 10 Plan

**Aevatar Team** · March 2, 2026

---

## 1. 市场运营交付

<div class="slide-meta"><span class="owner-tag">@Eanzhao</span> · <strong>市场运营</strong> · Due Friday 3/6 18:00</div>

在 2026-03-06 18:00 前交付 `channel-onboarding-v1.md`、`local-deploy-guide-v1.md`、`update-and-rollback-runbook-v1.md` ，周五演示。

- 目标权重: 40%
- 验收指标: 按文档本地从零部署 2 轮且中位耗时 <= 30 分钟
- 验收指标: 完成升级与回滚各 1 次并留存相关材料

***

<div class="slide-section-label">Quality Gate</div>

- **业务指标对齐：** 运营侧激活转化率提升、交付支持成本下降、系统可用性稳定。
- **交付物：**
  - `channel-onboarding-v1.md`
  - `local-deploy-guide-v1.md`
  - `update-and-rollback-runbook-v1.md`
  - 演示

---

## 2. Aevatar Mainnet SDK MVP

<div class="slide-meta"><span class="owner-tag">@Eanzhao</span> · <strong>SDK</strong> · Due Friday 3/6 18:00</div>

在 2026-03-06 18:00 前发布 `Aevatar Mainnet SDK MVP`（鉴权 + `/api/chat` + workflow 触发）并交付 `quickstart.md` 与可运行示例。

- 目标权重: 35%
- 验收指标: 在 2 个空项目场景下接入到首个成功调用 <= 30 分钟
- 验收指标: 3 个核心能力各连续 20 次调用成功率 >= 99%
- 验收指标: 示例项目可一键运行并附结果截图/日志链接

***

<div class="slide-section-label">Quality Gate</div>

- **业务指标对齐：** 开发者接入转化率提升、接入时长下降、生态扩展速度提升。
- **交付物：**
  - MVP (鉴权 + `/api/chat` + workflow 触发)
  - `quickstart.md` 及可运行示例

---

## 3. Workflow Demo 场景

<div class="slide-meta"><span class="owner-tag">@Eanzhao</span> · <strong>Workflow Demo</strong> · Due Friday 3/6 18:00</div>

在 2026-03-06 18:00 前交付 `demo-acceptance-checklist.md` 与固定演示脚本，覆盖六个关键场景。

- 目标权重: 20%
- 覆盖场景: SSE 基础可用、auto 进入审批、拒绝后再审批、通过后执行、auto_review 只定稿、WS 一致性与 `workflowYamls` 优先级
- 验收指标: 六场景 6/6 全通过，全链路连续 20 次演示成功率 >= 95%
- 验收指标: 周五现场 15 分钟内按脚本完整走通演示

***

<div class="slide-section-label">Quality Gate</div>

- **业务指标对齐：** 产品可信度与稳定性指标提升、售前/内部演示效率提升。
- **交付物：**
  - `demo-acceptance-checklist.md`
  - 固定演示脚本

---

## 4. Vibe 新版本迁移

<div class="slide-meta"><span class="owner-tag">@Eanzhao</span> · <strong>Vibe Researching</strong> · Due Friday 3/6 18:00</div>

在 2026-03-06 18:00 前交付 Vibe 新版本迁移结果与 `migration-notes-v1.md`（变更点/兼容边界/已知限制）。

- 目标权重: 5%
- 验收指标: 核心主流程 5 条回归用例通过率 100%
- 验收指标: 关键 API 切换完成率 100%
- 验收指标: 周五会议 5 分钟内可演示主流程

***

<div class="slide-section-label">Quality Gate</div>

- **业务指标对齐：** 历史项目维护成本下降、版本风险收敛、存量资产持续可用。
- **交付物：**
  - 迁移结果演示
  - `migration-notes-v1.md`
