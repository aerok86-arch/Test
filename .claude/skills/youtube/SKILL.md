---
name: youtube
description: Find the single best YouTube video for what the user needs, plus 3-4 solid alternatives. Use when the user asks to find a YouTube video, wants to learn something via video, or asks for video recommendations on any topic.
---

# YouTube Search Skill

Find the single best YouTube video for what the user needs, plus 3–4 solid alternatives.

---

## Core Principle

You picked one. Don't hedge. One primary recommendation, then alternatives. Confident tone throughout.

If the topic is ambiguous, interpret and go — don't ask for clarification first.

---

## Workflow

### Step 1: Interpret Intent

Before searching, assess:
- What is the user's expertise level? (beginner / intermediate / advanced)
- Do they want a quick overview or deep exploration?
- What content type fits best? (tutorial, explainer, lecture, walkthrough, review)

### Step 2: Run Multiple Searches

Run 3–4 distinct search queries using different angles and vocabulary — not just variations of the same phrasing.

Example for "Model Context Protocol":
- "Model Context Protocol explained"
- "MCP AI agents tutorial beginner"
- "MCP server setup walkthrough"
- "Claude MCP integration guide"

### Step 3: Evaluate Candidates

Pool results across all searches. Remove duplicates. Evaluate each on:
- **Relevance** — does it actually cover what was asked?
- **Channel credibility** — established creator or channel with track record
- **Duration** — appropriate for the requested depth
- **Recency** — prefer content within the last 12 months for fast-moving topics

**Exclude:**
- Shorts under 2 minutes
- Clickbait titles with no substance
- Duplicate channels in the final list
- Tangentially related content

### Step 4: Select and Present

Pick one primary recommendation. Choose 3–4 alternatives that each offer something meaningfully different — different depth, angle, channel style, or length.

---

## Output Format

```
**[Video Title]**
[Channel] · [Duration] · [Date]
[URL]
[One full sentence explaining why this is the best pick for what they asked]

---

**Also worth watching:**

**[Title]** — [Channel] · [Duration] · [URL]
[One short hook: what makes this one different]

**[Title]** — [Channel] · [Duration] · [URL]
[One short hook]

**[Title]** — [Channel] · [Duration] · [URL]
[One short hook]
```

---

## What to Avoid

- Narrating the search process ("I searched for X and found...")
- Hedging on the primary pick ("this might be good" / "you could try")
- Picking two videos from the same channel for alternatives
- Recommending Shorts as a primary result
- Asking clarifying questions before attempting a search
