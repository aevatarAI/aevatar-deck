# Aevatar Weekly Decks

Weekly progress presentations powered by Jekyll + reveal.js.

## Adding Your Goals for This Week

1. Open the current week's folder in `_decks/`. The folder is named by the Monday date:
   ```
   _decks/20260302-week10/
   ```

2. Edit **`plan.md`**. Each goal is a slide separated by `---`. Follow this format per goal:

   ```markdown
   ---

   ## Goal Title

   **Project Area** · Due Friday M/D

   One-sentence description of the deliverable.

   - Acceptance criterion 1
   - Acceptance criterion 2
   - Acceptance criterion 3
   ```

3. Commit and push to `main`. The site deploys automatically.

### Example goal slide

```markdown
---

## Paper Ingestion Agent

**Aevatar Mainnet** · Due Friday 3/6

Workflow G agent is merged to main and parses PDF and TeX papers into DAG nodes.

- PR merged to main
- ≥3 sample papers ingested end-to-end with 100% success rate
- Unlocks automated research input pipeline for end users
```

## Starting a New Week

1. Create a folder in `_decks/` named `yyyymmdd-week<N>` where the date is **Monday** of that week:
   ```
   _decks/20260309-week11/
   ```

2. Add the files:

   **`plan.md`** — Monday kickoff deck:
   ```yaml
   ---
   layout: deck
   title: "Week 11 Plan"
   date: 2026-03-09
   week: "2026-W11"
   type: plan
   ---

   ## Week 11 Plan

   **Aevatar Team** · March 9, 2026

   ---

   ## 1. Your First Goal

   ...
   ```

   **`review.md`** — Friday review deck (create when ready):
   ```yaml
   ---
   layout: deck
   title: "Week 11 Review"
   date: 2026-03-13
   week: "2026-W11"
   type: review
   ---
   ```

3. Author defaults to "Aevatar Team" automatically — no need to set it per file.

## Local Preview

```bash
bundle install
bundle exec jekyll serve
```

Visit [localhost:4000](http://localhost:4000). Click any deck to open the reveal.js presentation. Arrow keys to navigate slides.

## Slide Tips

- `---` separates horizontal slides
- `***` creates vertical (nested) sub-slides
- Standard Markdown: headings, lists, images, code blocks
- Each deck becomes its own reveal.js presentation

## Project Structure

```
_decks/
  20260302-week10/
    plan.md            → Monday planning deck
    review.md          → Friday review deck
_layouts/              → Jekyll layouts (default, deck, home)
assets/css/            → Custom styles (cyberpunk neon theme)
_config.yml            → Jekyll configuration
.github/workflows/     → GitHub Pages auto-deploy
```
