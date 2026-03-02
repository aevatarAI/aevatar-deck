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

## 1. 通用型交付 (Claw 化与本地部署)

<div class="slide-meta"><span class="owner-tag">@Eanzhao</span> · <strong>通用型</strong> · Due Friday 3/6 18:00</div>

本周五之前交付能够跑通的 Aevatar Localnet 核心能力验证环境与渠道连接指引，推动系统向 Claw 架构演进，并帮助运营侧实现在本地独立运转独立业务。

- 完成系统向 Claw 化结构重构的关键配置验证
- 重点打通并验证至少一个核心运营渠道 (Channel) 的接入
- 支持运营人员按向导在本地独立拉起 Aevatar Localnet 进行日常调测

***

<div class="slide-section-label">交付物</div>

- `channel-onboarding-v1.md`（运营渠道的 Claw 化接入指引与配置说明）
- `localnet-deploy-guide-v1.md`（Aevatar Localnet 开箱即用的本地部署指南）
- `update-and-rollback-runbook-v1.md`（系统更新升级及异常回滚手册）
- 最新版本的系统功能演示

***

<div class="slide-section-label">验收标准</div>

- 目标权重: 40%
- 成功接入 1 个运营 Channel 且 50 次请求连通成功率 ≥ 95%
- 运营人员按文档本地从零拉起 Localnet 耗时中位数 ≤ 30 分钟
- 从零到一完整完成一轮本地环境的升级与回滚流程

***

<div class="slide-section-label">战略对齐</div>

- 推动架构 Claw 化，提升系统灵活性与解耦能力
- 赋能运营侧快速开展自主接入与业务尝试，降低测试对接门槛
- 提升系统可用性并保证日常运行稳定

---

## 2. Aevatar Mainnet SDK MVP

<div class="slide-meta"><span class="owner-tag">@Eanzhao</span> · <strong>SDK</strong> · Due Friday 3/6 18:00</div>

本周五之前发布 Aevatar Mainnet SDK 的最小可用版本，支撑外部开发者快速完成应用鉴权、聊天对话和工作流触发。

- 跑通 SDK 的鉴权及核心 API（`/api/chat`）调用
- 支持跨项目环境快速通过工作流触发系统流程
- 提供快速开始指南和立即可用的官方代码示例

***

<div class="slide-section-label">交付物</div>

- SDK MVP（涵盖鉴权、通信、工作流等核心逻辑）
- `quickstart.md`（开发者快速入门接入文档及代码片）
- 一个能立即跑通运行的 Demo 项目示例代码

***

<div class="slide-section-label">验收标准</div>

- 目标权重: 35%
- 两个全新的空项目场景接入并跑通首次调用 ≤ 30 分钟
- 3 个核心能力各连续 20 次调用成功率 ≥ 99%
- 官方提供示例项目能够一键启动运行且无报错

***

<div class="slide-section-label">战略对齐</div>

- 提升外部开发者接入意愿和转化率
- 降低代码门槛，缩短平均接入时长
- 利用工具包加速生态应用和插件扩展速度

---

## 3. Workflow Demo 场景

<div class="slide-meta"><span class="owner-tag">@Eanzhao</span> · <strong>Workflow Demo</strong> · Due Friday 3/6 18:00</div>

本周五之前交付一套包含 6 个关键应用场景的演示脚本，在不接触底层代码的情况下完成所有链路呈现。

- 涵盖连接打通、自动审批流、循环打回、结果执行等工作流业务
- 基于标准化 YAML 实现快速验证业务配置
- 系统交互保证稳定运行

***

<div class="slide-section-label">交付物</div>

- `demo-acceptance-checklist.md`（六个关键演示场景对应的详细执行步骤和预期结果）
- 固定演示脚本（用于保证全流程连贯展示的操作口令与输入模板）

***

<div class="slide-section-label">验收标准</div>

- 目标权重: 25%
- 六个指定场景（SSE、auto 进入审批等）6/6 全部通过测试
- 全链路连续 20 次重复演示的成功率 ≥ 95%
- 周五规定会议 15 分钟内可按固定脚本顺畅走通并呈现结果

***

<div class="slide-section-label">战略对齐</div>

- 通过稳定可视化的演示提升产品可信度
- 为售前与内部方案支持提供直接生产工具，提升演示效率