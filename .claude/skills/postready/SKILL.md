---
name: postready
description: Run source material through a full four-step pipeline — draft posts, fact-check, tighten, HR screen — and deliver publication-ready LinkedIn posts without pauses. Use when the user types /postready, says "make this publish-ready", "run the full pipeline", or shares source material requesting finished posts.
---

# Post-Ready Pipeline

Automate a four-step content pipeline that transforms source material into publication-ready LinkedIn posts without pauses or checkpoints.

---

## Activation Triggers

- User types `/postready`
- "Make this publish-ready" / "run the full pipeline"
- User shares source content (PDF, email, newsletter, URL, notes) requesting finished, ready-to-post output

---

## The Four-Step Process

### Step 1: Content Generation

- Ingest source material and identify 3–4 strong angles (hot take, surprising stat, practical tip, story/narrative)
- Draft full-length posts matching the user's voice (use the `post` skill's voice profile)
- **Skip** the internal factcheck that the `content` skill normally includes — Step 2 handles it
- **Do not present drafts** — pass them directly to Step 2

### Step 2: Fact-Checking (Standard Tier)

- Run Standard-tier verification on posts containing statistics, named entities, historical claims, or attributed research
- **Do not show the tier-selection menu** — always use Standard
- Apply suggested fixes for ❌ incorrect and ⚠️ partially correct findings
- Document fixes briefly (e.g., "Post 2: removed unsourced claim about X")
- Note posts with no checkable claims and pass through unchanged
- **Do not present intermediate drafts** — feed corrected posts to Step 3

### Step 3: Tightening (Hatchet)

- Target ~50% length reduction
- Preserve already-tight posts — don't over-cut
- Keep sharp openings and intentional line breaks for rhythm
- Maintain the user's voice throughout
- **Do not present** — feed tightened posts to Step 4

### Step 4: HR Screening

Apply verdicts from the `ask-hr` skill:

| Verdict | Action |
|---|---|
| ✅ Clear / 🟢 Low Risk | Keep as-is |
| 🟡 Moderate Risk | Apply Full Rewrite |
| 🔴 High Risk | Apply Full Rewrite + flag prominently |

Document only the issue and severity — not full risk tables or detailed breakdowns.

---

## Final Output Format

Present all posts together with angle labels:

```
**Post 1 — [Angle Type]**
[Final post content]

**Post 2 — [Angle Type]**
[Final post content]

[etc.]

---

**Pipeline Notes**
- Factcheck: [brief summary of fixes, or "No issues found"]
- Hatchet: [brief reduction summary, e.g., "Posts trimmed ~45–55%"]
- HR: [flags if any, or "All posts cleared"]
```

Close by asking which posts the user wants to adjust.

---

## Critical Constraints

- **Never pause between steps** — run all four steps end-to-end
- **Never show intermediate drafts** — only present final versions
- **Always use Standard factcheck tier** — no exceptions
- **Run all four steps on every post** — no skipping
- **Omit detailed risk tables** and full claim-by-claim factcheck reports from final notes
- **Do not open posts with newsletter framing** ("This week's newsletter...", "I wrote about...")
