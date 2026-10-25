---
name: problem-discovery-funnel
description: Collect real-world problem signals with high recall, review them against a chosen research direction, and promote supported findings into auditable verified problem nodes. Use for problem discovery, pain-point mining, incident or interview intake, evidence review, or maintaining a problem library. Do not use to generate solutions, products, startup ideas, business plans, or investment judgments.
---

# Problem Discovery Funnel

Build an evidence-traceable problem library with a **wide entrance and strict promotion gates**. Preserve strange, weak, contradictory, and disproven claims so the library records how knowledge changed.

## Non-negotiable boundary

Investigate problems only. Do not propose solutions, product concepts, feature designs, business plans, market opportunities, or investment judgments. When source material contains a proposed solution, extract only its underlying problem assumptions and evidence claims.

Never invent URLs, identifiers, standards, incidents, cases, or quantitative results. Write `待核实` or `待测定` when the evidence does not support a precise claim.

## Route the request

Choose the stage from the user's intent:

1. **Open collection** — default when the user supplies raw material or asks to discover or collect problems. Read [references/01-open-collection.md](references/01-open-collection.md). Optimize recall; do not filter for plausibility, scale, evidence quality, or commercial value.
2. **Directional review** — use only when the user gives a research direction or asks to search, compare, shortlist, deduplicate, or assess an existing candidate pool. Read [references/02-directional-review.md](references/02-directional-review.md) and [references/evidence-taxonomy.md](references/evidence-taxonomy.md).
3. **Strict verification** — use only when the user asks to verify, audit, formalize, or promote candidates into the verified library. Read [references/03-strict-verification.md](references/03-strict-verification.md) and [references/evidence-taxonomy.md](references/evidence-taxonomy.md).

If the request spans stages, complete them in order and keep each stage's output separate. Do not silently promote a candidate because it sounds credible.

## Library layout

Store records under `problem-library/` when the user asks to persist them:

- `01-candidate-pool/`: raw candidate cards; append-only except for explicit corrections and metadata.
- `02-directional-review/`: review records tied to a stated direction, including non-adopted candidates and reasons.
- `03-verified-nodes/`: formal problem nodes with evidence, counterevidence, relationships, and revision history.

Use one Markdown file per record. Filenames should begin with the record ID. Preserve links from verified nodes back to every contributing candidate and review. Never move or delete an earlier-stage record merely because a later stage rejected or disproved it.

Before writing, inspect the relevant directory to avoid ID collisions and duplicate records. If the user did not ask to save results, return the appropriate schema in chat without changing the library.

## Shared epistemic rules

- Separate observation, source interpretation, and researcher inference.
- Prefix every unverified causal or cross-domain inference with `[假设]`.
- Absence of located evidence is not evidence of absence.
- Treat social posts, anonymous comments, PR, vendor white papers, and SEO content as leads rather than confirmation.
- Prefer primary operational evidence. Record exactly what a source supports and what it does not support.
- Keep contrary evidence, scope limits, unresolved questions, dependencies, near-duplicates, and historical status changes.
- Never use venture trends, algorithm popularity, market size, or monetization potential as retention criteria.

## Default behavior

When stage or direction is unclear, perform **Stage 1 only**. Capture broadly, identify missing context, and stop before judging validity or importance. Ask for a research direction only when the user requests Stage 2 and none can be inferred safely.
