---
layout: deck
title: "Week 11 Plan"
date: 2026-03-09
week: "2026-W11"
type: plan
member: Potter
---

## Week 11 Plan

**Aevatar Team** · March 9, 2026

---

## 1. 修改调整并提审 NyxID 安卓版本

<div class="slide-meta"><span class="weight-badge">50%</span> <span class="owner-tag">@Potter</span> · <strong>NyxID Mobile (Android)</strong> · Due Friday 3/13</div>

<div class="slide-section-label">具体内容</div>

- 本周五（2026-03-13）前完成 NyxID Android 版本的修改调整、回归验证与提审
- 完成提审前问题收敛与必要调整（功能、交互、稳定性）
- 完成核心链路回归：Inbox → Detail → Approve / Deny → 回传
- 输出提审包并完成审核提交流程

***

<div class="slide-section-label">交付物</div>

- Android 提审记录（版本号、提审时间、审核状态）
- 核心路径回归测试结果

***

<div class="slide-section-label">验收标准</div>

- 阻塞问题清零（P0/P1 = 0）
- 核心链路回归通过率 100%
- 安卓版本提审提交完成

---

## 2. 增加 NyxID App 功能：Approval History 与 Active Grants

<div class="slide-meta"><span class="weight-badge">50%</span> <span class="owner-tag">@Potter</span> · <strong>NyxID App</strong> · Due Friday 3/13</div>

<div class="slide-section-label">具体内容</div>

- 在 NyxID App 中新增审批历史与生效授权模块，提升授权过程可视化与可管理性
- 新增 `Approval History` 模块：展示请求信息、审批状态、请求时间、决策时间
- 新增 `Active Grants` 模块：展示当前生效授权及空态
- 完成接口联调与状态处理（加载态、错误态、空态）

### 参考界面（Approval History）

![Approval History]({{ '/assets/images/week11-review-potter-approval-history.png' | relative_url }})

***

### 参考界面（Active Grants）

![Active Grants]({{ '/assets/images/week11-review-potter-active-grants.png' | relative_url }})

***

<div class="slide-section-label">交付物</div>

- `Approval History` 可用页面（列表与状态展示）
- `Active Grants` 可用页面（含空态展示）
- 接口字段与联调说明

***

<div class="slide-section-label">验收标准</div>

- 两个模块在联调环境可稳定访问并正确渲染
- 状态展示正确（Approved / Rejected / Expired）
- 空态、加载态、错误态均可用
