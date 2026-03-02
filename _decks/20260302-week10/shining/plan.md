---
layout: deck
title: "Week 10 Plan"
date: 2026-03-02
week: "2026-W10"
type: plan
member: Shining
---

## Week 10 Plan

**Aevatar Team** · March 2, 2026

---

## 1. Paper Ingestion Agent

<div class="slide-meta"><span class="owner-tag">@Shining</span> · <strong>Aevatar Mainnet</strong> · Due Friday 3/6</div>

Workflow G agent is merged to main and successfully parses PDF and TeX research papers into DAG nodes.

- Parse PDF papers via layout-aware extraction
- Parse TeX papers via source-level AST parsing
- Map extracted sections, claims, and references into DAG nodes
- Supports mainnet product completeness — unlocks automated research input pipeline for end users

***

<div class="slide-section-label">Quality Gate</div>

- PR merged to main
- ≥3 sample papers (PDF + TeX) ingested end-to-end with 100 % DAG node creation success rate
- All extracted DAG nodes contain valid title, content, and source-reference fields
- No regressions on existing workflow tests

***

### Current — Workflow Research UI

![Current Workflow UI]({{ '/assets/images/current-workflow-ui.png' | relative_url }})

***

### Proposed — With Paper Ingestion

<div style="display: flex; gap: 1rem; font-size: 0.55em; line-height: 1.4;">
<div style="flex: 1; background: #1a1a2e; border: 1px solid rgba(0,240,255,0.2); border-radius: 6px; padding: 1rem;">
<div style="color: #00f0ff; font-weight: 700; margin-bottom: 0.5rem;">📄 Paper Ingestion</div>
<div style="border: 1px dashed rgba(0,240,255,0.3); border-radius: 4px; padding: 0.8rem; text-align: center; margin-bottom: 0.8rem; color: #6a6a8a;">
Drop PDF or TeX files here<br>or click to browse
</div>
<div style="color: #6a6a8a; font-size: 0.9em; margin-bottom: 0.3rem;">Ingested Papers:</div>
<div style="background: #12121a; border-radius: 4px; padding: 0.5rem; margin-bottom: 0.3rem;">
<span style="color: #39ff14;">✓</span> <span style="color: #e0e0f0;">attention_is_all_you_need.pdf</span><br>
<span style="color: #6a6a8a; font-size: 0.85em;">→ 12 DAG nodes created</span>
</div>
<div style="background: #12121a; border-radius: 4px; padding: 0.5rem; margin-bottom: 0.3rem;">
<span style="color: #39ff14;">✓</span> <span style="color: #e0e0f0;">bert_pretraining.tex</span><br>
<span style="color: #6a6a8a; font-size: 0.85em;">→ 8 DAG nodes created</span>
</div>
<div style="background: #12121a; border-radius: 4px; padding: 0.5rem;">
<span style="color: #ff00aa;">⟳</span> <span style="color: #e0e0f0;">gpt4_technical_report.pdf</span><br>
<span style="color: #6a6a8a; font-size: 0.85em;">→ Parsing... 64%</span>
</div>
</div>
<div style="flex: 1.5; background: #1a1a2e; border: 1px solid rgba(0,240,255,0.2); border-radius: 6px; padding: 1rem;">
<div style="color: #00f0ff; font-weight: 700; margin-bottom: 0.5rem;">🔬 Research Session</div>
<div style="color: #e0e0f0; margin-bottom: 0.5rem;">Knowledge graph populated from ingested papers. Research agent can now reference extracted claims and findings.</div>
<div style="background: #12121a; border-radius: 4px; padding: 0.8rem; margin-bottom: 0.5rem;">
<span style="color: #b44aff;">Agent:</span> <span style="color: #e0e0f0;">Found 3 related claims from ingested papers about transformer scaling laws...</span>
</div>
<div style="background: #0a0a0f; border: 1px solid rgba(0,240,255,0.15); border-radius: 4px; padding: 0.5rem; color: #6a6a8a;">
Enter research topic...
</div>
</div>
</div>

---

## 2. Context Size Solution

<div class="slide-meta"><span class="owner-tag">@Shining</span> · <strong>Aevatar Mainnet</strong> · Due Friday 3/6</div>

Full-graph context overflow is resolved; automated follow-up research sessions run without context limit failures.

- Implement sliding-window or summarization strategy for large graphs
- Agent receives pruned context that preserves key claims and structure
- Automated follow-up sessions complete without context limit errors
- Improves platform stability and user retention

***

<div class="slide-section-label">Quality Gate</div>

- Technical design doc reviewed and approved
- Prototype passes on a graph with ≥50 nodes without exceeding context limit
- Research session failure rate reduced from current baseline to <5 %
- No degradation in answer quality vs. small-graph baseline

---

## 3. Argo CD Auto Deployment Pipeline

<div class="slide-meta"><span class="owner-tag">@Shining</span> · <strong>DevOps</strong> · Due Friday 3/6</div>

Argo CD pipelines are operational for Aevatar, DAG, Notification, and Storage services on staging.

- Configure Argo CD application manifests for all 4 services
- Set up Git-based sync with auto-deploy on merge to main
- Add health checks and rollback policies per service
- Reduces manual ops cost and deployment errors — supports developer velocity

***

<div class="slide-section-label">Quality Gate</div>

- All 4 services deployed and verified via Argo CD on staging
- Average deployment time <10 min per service
- Rollback successfully tested on at least 1 service
- Runbook documented for on-call engineers

---

## 4. Mobile Permission Management

<div class="slide-meta"><span class="owner-tag">@Shining</span> · <strong>NyxID</strong> · Due Friday 3/6</div>

Permission management for NyxID mobile app is production-ready and merged.

- Implement create, read, update, delete flows for permission groups
- Integrate with backend RBAC API
- Handle edge cases: offline state, permission conflicts, role inheritance
- Unblocks NyxID mobile launch — supports user conversion funnel

***

<div class="slide-section-label">Quality Gate</div>

- All permission CRUD flows pass QA with 0 blocking bugs
- Code reviewed and merged to main
- UI matches approved Figma specs with ≤2 minor deviations
- Permission changes reflected in real-time without app restart

---

## 5. User Workflow Upload

<div class="slide-meta"><span class="owner-tag">@Shining</span> · <strong>Aevatar Mainnet</strong> · Due Friday 3/6</div>

Users can upload and execute custom workflows on mainnet staging.

- Build upload endpoint with file validation and versioning
- Wire upload → parse → execute pipeline end-to-end
- Surface execution status and results in the UI
- Core platform feature for user acquisition and ecosystem expansion — tied to ARR growth

***

<div class="slide-section-label">Quality Gate</div>

- Upload → execute flow verified end-to-end on staging
- ≥2 test workflows uploaded and executed successfully
- Invalid workflow uploads rejected with clear error messages
- Execution logs accessible to the uploading user
