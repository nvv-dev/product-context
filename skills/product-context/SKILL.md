---
name: product-context
description: Use when starting marketing, copy, design, SEO or sales work for a product, or when the user shares new facts about the product, its customers, positioning, objections or results. Creates and maintains .agents/product-context.md, the single versioned file that copy, content, design and SEO work read instead of asking the same questions again. If the file exists, summarizes it and updates only what was asked.
---

# Product context

Every piece of marketing work needs the same facts: what the product is, who it is for, why they would choose it and what proves it. Asking for them in every session wastes the owner's time and produces drift between pages. Keep them in one file, `.agents/product-context.md`, that other skills and agents read first.

## If the file does not exist

1. Ask the owner for the facts below, a few questions at a time, starting with what the product is and who pays for it. Accept "unknown" as an answer and record it as an open question; never fill a gap with a guess.
2. Read what is already in the repo (README, landing pages, specs, store listings) and propose answers for the owner to confirm. A proposal is not a fact until the owner confirms it.
3. Write the file with the structure below, version `1.0.0`, and one changelog line.

## If the file exists

1. Read it and give the owner a summary of five lines at most: product, ideal customer, main promise, strongest proof, open questions.
2. Change only the sections the owner asked about. Do not rewrite, reorder or "improve" anything else.
3. Bump the version (major: new positioning or ideal customer; minor: a new section, objection, proof or learning; patch: wording) and add a changelog line with the date and what changed.

## Structure

```markdown
# Product context — <product name>
Version: 1.2.0 · Updated: 2026-10-27 · Owner: <name>

## Product
What it is in one sentence, what it does, price model, platforms, status (idea, beta, live).

## Ideal customer
Who buys, who uses (if different), their situation, the job they hire the product for, and who it is NOT for.

## Problem and alternatives
The pain in the customer's own words, and what they use today instead (including "nothing" or a spreadsheet).

## Positioning
Category, main promise, two or three differentiators against the real alternatives, and the tone.

## Objections
Each objection the customer raises, with the answer and the proof that backs it.

## Proof
Only verifiable items: numbers with source and date, approved testimonials with permission recorded, client names with permission, certifications, demos. Mark each one approved or pending.

## Customer language
Exact phrases customers use, with where they were heard (call, review, support ticket).

## Learnings
What was tried, the result and the date (page tests, campaigns, launches).

## Open questions
Facts nobody has confirmed yet.

## Changelog
- 1.2.0 · 2026-10-27 · Added objection about pricing with case study as proof.
```

## Rules

- Facts come from the owner, real customers or verifiable data. Mark anything else as an assumption or leave it in open questions.
- Never invent numbers, testimonials, client names or logos. A proof item without source or permission stays "pending" and must not be used in public copy.
- Customer language is quoted as heard; do not polish it.
- No personal data about customers beyond what the owner has permission to keep (no emails, phone numbers or private messages).
- One product per file. For several products, use `.agents/product-context-<slug>.md` and say which one each task uses.

## Output

The path of the file, its version, the summary, and the list of open questions.

## Known failures

_Record real mistakes here with a date and the rule that prevents them._
