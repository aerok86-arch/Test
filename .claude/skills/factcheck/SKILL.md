---
name: factcheck
description: Verify factual claims in written content — statistics, attributions, dates, named entities — and return a sourced claim-by-claim report with fixes and publishability ratings. Use when the user types /factcheck, pastes content requesting verification, or asks to "check facts", "verify accuracy", or "is this true".
---

# Fact Checker

Verify factual claims in written content and return a sourced, claim-by-claim report with fixes and a publishability rating.

---

## Activation Triggers
- User types `/factcheck`
- User pastes content requesting verification ("fact-check this," "verify," "is this accurate?")

---

## Workflow

### Step 1: Gather Input

Request content if missing. If verification tier is unspecified, ask with clickable options:
- ⚡ **Quick** — Top 3–5 claims, one search per claim, prioritizes speed
- 🔍 **Standard** — All claims, 1–2 searches each, authoritative sources emphasized
- 🧠 **Deep** — All claims, 2–4 searches per claim, mandatory secondary verification, flags nuance and context

### Step 2: Extract Claims

Identify all checkable factual statements: statistics, dates, attributions, scientific facts, historical claims. Label them C1, C2, etc. Flag anything that looks viral or misquoted for extra scrutiny.

### Step 3: Research by Tier

**⚡ Quick:** Focus on the highest-risk claims. One search each. Confirm surprises with a follow-up.

**🔍 Standard:** Check all claims. One to two searches each. Secondary verification for any unexpected findings. Emphasize authoritative sources (government data, peer-reviewed research, major news outlets with primary sourcing).

**🧠 Deep:** All claims, two to four searches each. Mandatory cross-verification for any uncertain result. Flag nuance, outdated data, and source conflicts.

### Step 4: Report

---

### 🔎 Fact-Check Report — [Tier]

**Publishability:** 🟢 Safe to publish / 🟡 Fix flagged items first / 🔴 Significant errors — do not publish as-is

---

For each claim:

**C[N]: [claim as written]**
- **Status:** [✅ / ❌ / ⚠️ / ❓ / 🚨]
- **Finding:** [1–3 sentence explanation with source]
- **Source:** [URL or citation]
- **Fix:** [Only for ❌ and ⚠️ — corrected version of the claim]

---

**Summary:** [Claim counts by status] + [2 sentence overall assessment]

---

## Status Labels

| Label | Meaning |
|---|---|
| ✅ Verified | Confirmed by reliable sources |
| ❌ Incorrect | Contradicted — correction provided |
| ⚠️ Partially correct | True but missing context or outdated |
| ❓ Unverifiable | No reliable sources found |
| 🚨 Viral/Misquoted | Widely circulated but unreliable origin |

## Publishability Ratings

- 🟢 **Safe to publish** — All claims verified or unverifiable but low-stakes
- 🟡 **Fix flagged items first** — Some errors or gaps that should be corrected
- 🔴 **Do not publish** — Significant factual errors that would undermine credibility
