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

<div class="slide-meta"><span class="weight-badge">25%</span> <span class="owner-tag">@Shining</span> · <strong>Aevatar Mainnet</strong> · Due Friday 3/6</div>

<div class="slide-section-label">Description</div>

- Workflow G agent parses PDF + TeX papers into DAG nodes
- PDF layout-aware extraction + TeX AST parsing
- Extracted sections/claims mapped to DAG nodes

<div class="slide-section-label">Quality Gate</div>

- PR merged to main
- ≥3 papers ingested with 100% DAG node success rate

***

### Current UI

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
<div style="color: #e0e0f0; margin-bottom: 0.5rem;">Knowledge graph populated from ingested papers.</div>
<div style="background: #12121a; border-radius: 4px; padding: 0.8rem; margin-bottom: 0.5rem;">
<span style="color: #b44aff;">Agent:</span> <span style="color: #e0e0f0;">Found 3 related claims about transformer scaling laws...</span>
</div>
<div style="background: #0a0a0f; border: 1px solid rgba(0,240,255,0.15); border-radius: 4px; padding: 0.5rem; color: #6a6a8a;">
Enter research topic...
</div>
</div>
</div>

---

## 2. Context Size Solution

<div class="slide-meta"><span class="weight-badge">40%</span> <span class="owner-tag">@Shining</span> · <strong>Aevatar Mainnet</strong> · Due Friday 3/6</div>

<div class="slide-section-label">Description</div>

- Resolve full-graph context overflow for large graphs
- Sliding-window / summarization strategy
- Follow-up sessions complete without context errors

<div class="slide-section-label">Quality Gate</div>

- Design doc approved
- Passes on graph with ≥50 nodes
- Session failure rate < 5%

---

## 3. Auto Paper Generation

<div class="slide-meta"><span class="weight-badge">25%</span> <span class="owner-tag">@Shining</span> · <strong>Aevatar Mainnet</strong> · Due Friday 3/6</div>

<div class="slide-section-label">Description</div>

- Click any node on the knowledge graph to trigger paper generation
- Integrated with Workflow G agent to produce research paper from DAG context
- Auto-assembles related claims, evidence, and citations into structured output

<div class="slide-section-label">Quality Gate</div>

- Node-click → generation pipeline works e2e
- Generated paper includes correct citations from source nodes
- ≥2 papers generated from different graph regions

---

## 4. User Workflow Upload

<div class="slide-meta"><span class="weight-badge">10%</span> <span class="owner-tag">@Shining</span> · <strong>Aevatar Mainnet</strong> · Due Friday 3/6</div>

<div class="slide-section-label">Description</div>

- Upload + execute custom workflows on mainnet staging
- Upload endpoint with validation + versioning
- Upload → parse → execute pipeline e2e

<div class="slide-section-label">Quality Gate</div>

- E2e verified on staging
- ≥2 workflows uploaded and executed
- Invalid uploads rejected with clear errors
