---
layout: deck
title: "Week 11 Review"
date: 2026-03-13
week: "2026-W11"
type: review
member: Potter
---

## Week 11 Review

**Aevatar Team** · March 13, 2026

---

## 1. NyxID 双端应用商店发布与授权体验补齐

<div class="slide-meta"><span class="owner-tag">@Potter</span> · <strong>NyxID</strong></div>

- 完成 NyxID iOS / Android 双端应用商店发布，发布链路已打通
- 完成 `Approval History` 与 `Active Grants` 两个核心页面，补齐授权可见性与状态管理
- 核心链路保持可用：Inbox → Detail → Approve / Deny → 回传

***

### Approval History

<div style="display: flex; justify-content: center; align-items: flex-start; height: 60vh;">
<img src="{{ '/assets/images/week11-review-potter-approval-history.png' | relative_url }}" alt="Approval History" style="max-height: 55vh;">
</div>

***

### Active Grants

<div style="display: flex; justify-content: center; align-items: flex-start; height: 60vh;">
<img src="{{ '/assets/images/week11-review-potter-active-grants.png' | relative_url }}" alt="Active Grants" style="max-height: 55vh;">
</div>

---

## 2. Aevatar SDK 开发完成并对齐服务能力

<div class="slide-meta"><span class="owner-tag">@Potter</span> · <strong>Aevatar SDK</strong></div>

- 完成 Aevatar SDK 主体开发，沉淀统一的调用入口与对象封装
- 对齐 Aevatar 服务能力边界、接口约定与数据结构，降低前后端联调成本
- 为 Console 和后续业务接入提供可复用的 SDK 基座

***

<div class="slide-section-label">本周交付</div>

- SDK 开发完成，可支撑 Aevatar 服务接入
- 服务侧能力映射完成，关键对象与调用路径已统一
- 为 `Workflows` / `Actors` / `Runs` 模块接入打下基础

---

## 3. Aevatar Console 完成整体项目搭建

<div class="slide-meta"><span class="owner-tag">@Potter</span> · <strong>Aevatar Console</strong></div>

- 完成 Aevatar Console 整体项目初始化、基础布局与导航框架
- 落地首批核心模块：`Workflows`、`Actors`、`Runs`
- 建立面向 Aevatar 服务的交互入口，为后续 Console 能力扩展提供基础

***

### Workflows

<div style="display: flex; justify-content: center; align-items: flex-start; height: 56vh;">
<img src="{{ '/assets/images/week11-review-potter-console-workflows.png' | relative_url }}" alt="Aevatar Console Workflows" style="max-height: 52vh;">
</div>

- 支持浏览 workflow library、查看 workflow detail，并直接进入 run
- 建立 YAML / Roles / Steps / Graph / Run 等基础查看入口

***

### Actors

<div style="display: flex; justify-content: center; align-items: flex-start; height: 56vh;">
<img src="{{ '/assets/images/week11-review-potter-console-actors.png' | relative_url }}" alt="Aevatar Console Actors" style="max-height: 52vh;">
</div>

- 支持按 actorId 与图查询参数加载 actor snapshot
- 为执行历史、拓扑与 graph 观察能力建立模块入口

***

### Runs

<div style="display: flex; justify-content: center; align-items: flex-start; height: 56vh;">
<img src="{{ '/assets/images/week11-review-potter-console-runs.png' | relative_url }}" alt="Aevatar Console Runs" style="max-height: 52vh;">
</div>

- 支持从 Console 发起 workflow run，并展示当前 run state
- 预留 human interaction 区域，完成运行态与交互态的首版框架

---

## 4. Summary

<div class="slide-meta"><span class="owner-tag">@Potter</span> · <strong>Week 11</strong></div>

- NyxID 完成双端应用商店发布，并补齐授权管理关键页面
- Aevatar SDK 开发完成并完成服务侧对齐
- Aevatar Console 从 0 到 1 完成整体项目搭建，交付 Workflows / Actors / Runs 三个核心模块
