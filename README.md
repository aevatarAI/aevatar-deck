# Aevatar Weekly Decks

Weekly progress presentations powered by Jekyll + reveal.js. Cyberpunk neon theme, auto-deployed to GitHub Pages.

**Live site:** [aevatarAI.github.io/aevatar-deck](https://aevatarAI.github.io/aevatar-deck)

## Adding Your Plan for This Week

1. Find your folder under the current week in `_decks/`. Each member has their own subfolder:
   ```
   _decks/20260302-week10/
     shining/plan.md
     ean/plan.md
     louis/plan.md
   ```

2. If your folder doesn't exist, create it and add `plan.md` with this front matter:
   ```yaml
   ---
   layout: deck
   title: "Week 10 Plan"
   date: 2026-03-02
   week: "2026-W10"
   type: plan
   member: YourName
   ---
   ```

3. Write your slides. Each task is separated by `---` and follows this structure:

   ```markdown
   ---

   ## 1. Task Title

   <div class="slide-meta"><span class="weight-badge">25%</span> <span class="owner-tag">@YourName</span> · <strong>Project Area</strong> · Due Friday 3/6</div>

   <div class="slide-section-label">Description</div>

   - What you're building / delivering
   - Key technical details

   <div class="slide-section-label">Quality Gate</div>

   - Acceptance criterion 1
   - Acceptance criterion 2
   ```

4. Commit and push to `main`. The site deploys automatically via GitHub Actions.

### Slide elements explained

| Element | Purpose |
|---------|---------|
| `<span class="weight-badge">25%</span>` | Task weight percentage (cyan pill) |
| `<span class="owner-tag">@Name</span>` | Owner tag (gold badge) |
| `<div class="slide-section-label">...</div>` | Section header (green label — "Description", "Quality Gate") |
| `<div class="slide-meta">...</div>` | Metadata line below the heading |

## Starting a New Week

1. Create a folder named `yyyymmdd-weekN` where the date is **Monday** of that week:
   ```
   _decks/20260309-week11/
   ```

2. Each member creates their own subfolder with `plan.md`:
   ```
   _decks/20260309-week11/yourname/plan.md
   ```

3. Front matter template:
   ```yaml
   ---
   layout: deck
   title: "Week 11 Plan"
   date: 2026-03-09
   week: "2026-W11"
   type: plan
   member: YourName
   ---

   ## Week 11 Plan

   **Aevatar Team** · March 9, 2026

   ---

   ## 1. First Task

   <div class="slide-meta"><span class="weight-badge">40%</span> <span class="owner-tag">@YourName</span> · <strong>Project</strong> · Due Friday 3/13</div>

   <div class="slide-section-label">Description</div>

   - ...

   <div class="slide-section-label">Quality Gate</div>

   - ...
   ```

4. For a Friday review deck, add `review.md` in your folder with `type: review` and the Friday date.

## Local Preview

```bash
make install   # first time only
make serve     # starts local server
```

Visit [localhost:4000](http://localhost:4000). Click any deck to open the reveal.js presentation. Arrow keys navigate slides.

## Slide Tips

- `---` separates horizontal slides
- `***` creates vertical (nested) sub-slides within a slide
- Standard Markdown works: headings, lists, images, code blocks
- HTML `<div>` elements for metadata, labels, and mockups must be outside markdown blocks
- Task weights across all your items should total 100%

## Project Structure

```
_decks/
  20260302-week10/
    shining/plan.md      → Shining's planning deck
    ean/plan.md          → Ean's planning deck
    louis/plan.md        → Louis's planning deck
_layouts/
  default.html           → Base HTML shell
  deck.html              → reveal.js presentation wrapper
  home.html              → Index page with expandable week/member list
assets/
  css/style.css          → Cyberpunk neon theme
  images/                → Screenshots and diagrams
_config.yml              → Jekyll config (collections, team members, defaults)
Makefile                 → Local dev shortcuts (make serve, make build)
.github/workflows/       → GitHub Pages auto-deploy on push to main
```

## Team Members

Shining · Ean · Louis · Potter · Haylee · Kai Wei · Kai Huei
