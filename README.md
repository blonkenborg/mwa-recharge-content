# eGYM Recharge — Educational Content Repo

This repo stores all educational articles shown in the **eGYM Recharge** app. Content is authored here, reviewed by Hannah R., and automatically compiled into a JSON feed the app consumes.

---

## How content gets into the app

```
Article written (by team or AI agent)
        ↓
Pull Request opened
        ↓
Hannah R. reviews and approves
        ↓
Merged to main
        ↓
GitHub Action compiles → content.json (auto)
        ↓
App fetches content.json at runtime
```

---

## How to review an article (Hannah's guide)

1. Open the PR on GitHub
2. Read the article file in `articles/{tag}/{slug}.md`
3. Check:
   - Is the information accurate?
   - Is the tone right for our users? (direct, evidence-based, not preachy)
   - Does it connect to the eGYM / Recharge context?
   - Is the summary (2 sentences shown in the app card) compelling?
4. **Approve** if it's good to go
5. **Request changes** if it needs edits — leave specific comments on the lines to fix
6. **Close the PR** if the article shouldn't be published

You do not need to touch any code. Everything else is automatic.

---

## How to edit an article

Edit the `.md` file directly on GitHub (click the pencil icon), make your changes, and commit to the same branch. The PR will update automatically.

---

## Article structure

Each article lives at `articles/{category}/{slug}.md` and has:

```yaml
---
slug: unique-url-id
title: "Article title shown in the app"
summary: "Short description shown on the card"
tags:
  - one-of-the-allowed-tags
publishedAt: YYYY-MM-DD
relatedChallengeTypes:   # optional — links article to specific workout challenges
  - weeklySMWorkoutDays
---

Article body in Markdown...
```

**Allowed tags:** `habit-building`, `micro-habits`, `micro-workouts`, `motivation`, `behavioral-change`, `muscle-building`, `strength-benefits`, `routines`, `recovery`

---

## Folder structure

```
articles/
  habit-building/
  micro-workouts/
  micro-habits/
  motivation/
  behavioral-change/
  muscle-building/
  strength-benefits/
  routines/
  recovery/
content.json          ← auto-generated, do not edit manually
CLAUDE.md             ← AI agent instructions
```

---

## Questions?

Contact the dev team or open an issue in this repo.
