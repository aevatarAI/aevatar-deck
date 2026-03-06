---
layout: deck
title: "Week 10 Review"
date: 2026-03-06
week: "2026-W10"
type: review
member: Kaihuei
---

## Week 10 Review

**Aevatar Team** · March 6, 2026

---

## 1. 池子服务多账号上线并完成压测

<div class="slide-meta"><span class="owner-tag">@Kaihuei</span> · <strong>Pool Service</strong></div>

- 使用公司邮箱创建 5 个账号用于池子服务
- Aevatar 已接入池子服务，用于论文推理

***

### 池子服务账号管理

<div style="display: flex; justify-content: center; align-items: flex-start;">
<img src="{{ '/assets/images/week10-review-kaihuei-pool-accounts.png' | relative_url }}" alt="Chrono LLM Pool Service Accounts" style="max-height: 45vh;">
</div>

---

## 2. Codex 安装配置 SOP 发布

<div class="slide-meta"><span class="owner-tag">@Kaihuei</span> · <strong>Codex</strong></div>

- 发布 SOP v1.0：《Clash Verge 科学上网配置与 Codex 账号订阅及使用指南》
- 在青云香港节点搭建 vless + reality 代理，伪装微软流量，转发至新加坡
- 提供管理 Panel，已开通 8 个账号，分配给中国区 7 位同事

---

## 3. SoulGarden 核心监控告警上线

<div class="slide-meta"><span class="owner-tag">@Kaihuei</span> · <strong>SoulGarden</strong></div>

- 已配置 CPU 和 Memory 监控告警规则（阈值 80%）
- 告警通知已接入飞书群（SoulGarden Prod）

***

### 飞书告警通知

<div style="display: flex; justify-content: center; align-items: flex-start;">
<img src="{{ '/assets/images/week10-review-kaihuei-soulgarden-alert.png' | relative_url }}" alt="SoulGarden Lark Alert Notifications" style="max-height: 45vh;">
</div>
