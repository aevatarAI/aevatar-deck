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

<div style="font-size: 0.75em;" markdown="1">

## 1. Maker Verification Process Integrated into TeX Nodes Upload as well as Research Loop

<div class="slide-meta"><span class="weight-badge">50%</span> <span class="owner-tag">@Shining</span> · <strong>Sisyphus</strong> · Due Friday 3/13</div>

<div class="slide-section-label">Description</div>

- Introduce **black (verified strongly-typed) nodes** as the outcome of maker verification workflow on blue (purified strongly-typed) nodes, completing the full pipeline: red (raw) → blue (purified) → black (verified)
- Research loop process filters and takes black nodes in the DAG as the baseline context for research progression, instead of blue nodes

<div class="slide-section-label">Quality Gate</div>

- Blue → black node promotion on TeX upload
- Research loop consumes black nodes only
- E2e on staging

</div>

---

<div style="font-size: 0.7em;" markdown="1">

## 2. Ornn Platform Onboarding to NyxID

<div class="slide-meta"><span class="weight-badge">50%</span> <span class="owner-tag">@Shining</span> · <strong>Ornn / NyxID</strong> · Due Friday 3/13</div>

<div class="slide-section-label">Description</div>

- OAuth with NyxID
- Finalize platform web interface providing core skill browsing and upload
- Core skill service exposing skill-search, skill-upload and skill-build deployed and exposed as MCP tools under Nyx platform
- OpenSandbox deployed under Nyx platform for script/program execution as part of the skills

<div class="slide-section-label">Quality Gate</div>

- NyxID auth flow works e2e (login/logout/user mgmt)
- Skill service MCP tools accessible on Nyx platform
- OpenSandbox executes scripts via skill pipeline
- E2e on staging

</div>
