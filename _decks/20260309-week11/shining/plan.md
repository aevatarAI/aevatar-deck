---
layout: deck
title: "Week 11 Plan"
date: 2026-03-09
week: "2026-W11"
type: plan
member: Shining
---

## Week 11 Plan

**Aevatar Team** · March 9, 2026

---

<div style="font-size: 0.7em;" markdown="1">

## 1. Maker Verification into TeX Upload & Research Loop

<div class="slide-meta"><span class="owner-tag">@Shining</span> · <strong>Sisyphus</strong> · Due Friday 3/13</div>

<div class="slide-section-label">Description</div>

- Introduce **black (verified strongly-typed) nodes** as the outcome of maker verification workflow on blue nodes, completing the full pipeline: red (raw) → blue (purified) → black (verified)
- Research loop filters and takes black nodes in the DAG as baseline context for research progression, instead of blue nodes

<div class="slide-section-label">Acceptance Criteria</div>

- Blue → black promotion triggers on TeX upload; verified on staging
- Research loop returns only black nodes; zero blue-node leakage in research sessions
- Only maker-verified data enters the research pipeline

</div>

---

<div style="font-size: 0.65em;" markdown="1">

## 2. Ornn Platform Onboarding to NyxID

<div class="slide-meta"><span class="owner-tag">@Shining</span> · <strong>Ornn / NyxID</strong> · Due Friday 3/13</div>

<div class="slide-section-label">Description</div>

- OAuth with NyxID
- Finalize platform web interface providing core skill browsing and upload
- Core skill service exposing skill-search, skill-upload and skill-build deployed as MCP tools under Nyx platform
- OpenSandbox deployed under Nyx platform for script/program execution as part of the skills

<div class="slide-section-label">Acceptance Criteria</div>

- OAuth login/logout functional on staging; new users can register and authenticate via NyxID e2e
- Web UI serves skill browsing and upload; skills discoverable and uploadable through UI
- skill-search, skill-upload, skill-build callable as MCP tools on Nyx platform
- OpenSandbox executes scripts triggered by skills on staging

</div>
