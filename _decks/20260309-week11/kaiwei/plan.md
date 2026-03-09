---
layout: deck
title: "Week 11 Plan"
date: 2026-03-09
week: "2026-W11"
type: plan
member: Kai Wei
---

## Week 11 Plan

**Aevatar Team** · March 9, 2026

---

<div style="font-size: 0.7em;" markdown="1">

## 1. Twitter/X OAuth Proxy Service

<div class="slide-meta"><span class="owner-tag">@Kai Wei</span> · <strong>NyxID Platform</strong> · Due Friday 3/13</div>

<div class="slide-section-label">Description</div>

- Let users connect their Twitter/X account to NyxID so that NyxID can act on their behalf — for example, posting tweets without users having to leave the platform
- This turns NyxID into a **unified action layer**: one login, and you can reach all your social accounts through a single place

<div class="slide-section-label">Acceptance Criteria</div>

- Twitter/X OAuth consent flow fully functional (redirect, callback, token exchange)
- Access token securely stored and linked to user's NyxID account
- Proxy endpoint operational: users can post to Twitter/X through NyxID in staging
- Supports platform value by enabling NyxID as a unified action layer across social services

</div>

---

<div style="font-size: 0.65em;" markdown="1">

## 2. User Installation Node — Self-Hosted Secrets

<div class="slide-meta"><span class="owner-tag">@Kai Wei</span> · <strong>NyxID Platform</strong> · Due Friday 3/13</div>

<div class="slide-section-label">Description</div>

- Design and prototype a way for security-conscious users to **keep their own API keys on their own machine** (or a Cloudflare Worker) instead of handing them to us
- NyxID stays in control as the master orchestrator — it routes requests through the user's self-hosted node, so the user never has to give up their credentials
- This builds trust with power users and enterprises who need full control over their secrets

<div class="slide-section-label">Acceptance Criteria</div>

- Architecture document completed covering node registration, credential storage, and request proxying flow
- Working proof-of-concept deployed (Cloudflare Worker or local node)
- Prototype demonstrates NyxID master sending a request that routes through the user's node
- Supports user trust and enterprise adoption by giving users full control over their credentials

</div>
