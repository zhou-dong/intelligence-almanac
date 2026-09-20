# Working on this repo

`intelligence-almanac` is the fact-checking backbone for a separate narrative project called "alchemist-ai." Alchemist-ai tells a continuous story of intelligence evolving — first life, chemotaxis, multicellularity, synaptic/Hebbian learning, and (per remaining chapter titles) onward through temporal-difference learning, structural/visual learning, deep learning, and decision-making — with a recurring cast (e.g. the organism *Ikaria* spans ch2 into ch3; a character "Vera" appears by ch7).

This repo is not the story — it's the evidence layer under it. Each chapter has a facts file (`chN-title.md`) tagging every checkable claim **established** / **plausible** / **speculative**, catching narrative overclaims, and flagging errors in the script for later correction.

A sibling repo `grimoire` holds project-agnostic deep-time/biology facts (geologic eras, LUCA, domains of life) — general reference material belongs there, not duplicated here.

## Fact-check, don't defer

Actively verify checkable claims (dates, attributions, mechanisms, causal chains) rather than transcribing what's asserted — including claims or framing stated by the user in conversation. The purpose of this repo is to prevent narrative dramatization from being mistaken for established fact, so accepting a claim uncritically just because it was asserted confidently defeats the point. Flag disagreement or uncertainty explicitly, and keep using the established/plausible/speculative tagging already established in the chapter files.

The user is writing this content to learn the material, not from a position of expertise — they said so directly. So go further than just verifying: when correcting or adding something, explain *why* (the actual mechanism, the math, the source), not just tag established/plausible/speculative and move on.

## Chapter file structure

Every chapter's facts file must contain at least two sections, in this order near the top:

- `## Overview` — a plain-language summary of the chapter's content, so it can be scanned without reading the full fact breakdown.
- `## Math model` — the formula (if any) the chapter's mechanism is modeled with, stated explicitly, compared against the previous chapter's Math model section (what's reused vs. genuinely new), and closed with a plausibility/simplification caveat. Follow the pattern already established in ch0–ch2's Math model sections.

## Diagrams

Any tree/branching diagram in a chapter file gets two versions, labeled `**Simple:**` and `**Full (annotated — ...):**` (see ch2's LUCA and animal-branching trees for the pattern):

- **Simple** — the bare structure only, no inline notes, for a quick structural glance.
- **Full** — the same structure with inline `←` annotations calling out the specific facts worth surfacing at a glance (e.g. where a capability like learning first appears, what's genuinely new vs. reused from an earlier chapter).

## Current work

ch0, ch1, and ch2 already have both sections. ch3 (`ch3-when-weights-learn.md`) through ch7 are missing both and need them added. Currently working on ch3.
