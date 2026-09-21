# Facts — The First Thing Alive

*This file holds facts specific to this chapter.*

## Overview

This chapter opens in the ocean's darkness, sometime between the late Hadean and early Archean, at a deep-sea hydrothermal vent that has never seen sunlight. A single cell sits anchored to the rock at the vent's mouth — sessile, with no flagella or motor of any kind, because there's no need to move: the vent's warm, mineral-rich, chemically reducing water delivers everything it needs right where it's fixed. It survives by chemolithoautotrophy, pulling energy from inorganic chemistry — hydrogen, hydrogen sulfide, iron — and building itself from CO₂ rather than sugar. Its whole existence is local: it reacts only to chemistry touching its surface, with no way to sense anything beyond direct contact, and no internal signaling to speak of. When it grows large enough, it simply splits in two. This is the story's zero point — something unambiguously alive, feeding, dividing, but blind, still, and entirely local — the baseline every later chapter (movement, sensing, multicellularity, learning) will depart from.

## Early Earth (before life)

*This chapter's backdrop spans from the early Hadean (bombardment, before oceans exist) through to the vent scene itself, whose exact era — late Hadean vs. early Archean — is deliberately left vague per `§ Setting → Timing`. General facts about this period live in `../grimoire/geologic-time/hadean-eon.md` and `../grimoire/geologic-time/archean-eon.md` — see those files rather than duplicating here.*

## Setting

### Timing

- Whether this chapter's vent scene falls in the Hadean or the Archean is unresolved. Per `../grimoire/geologic-time/hadean-eon.md`, oceans are inferred to exist within the Hadean itself, not only starting in the Archean — so oceans, and therefore seafloor vents, could have existed well before the Archean even starts. (plausible)
- LUCA's usual placement (per `../grimoire/domains-of-life/luca.md`) sits right around or before the Hadean/Archean boundary — and per `§ Organism` / `§ Framing notes`, this organism's timing relative to LUCA is deliberately left vague (could be before, at, or after it). So the vent scene's era should stay vague for the same reason. (plausible)

### Location

- Deep-sea hydrothermal vents sit far below the ocean surface, past the depth sunlight penetrates; it has never depended on solar energy. General darkness/visual-environment facts live in `../grimoire/domains-of-life/luca.md § Environment → Visual` — see that file rather than duplicating here. (established — physical fact of ocean depth and light attenuation)

### Vent chemistry

- Deep-sea hydrothermal vents are warm, mineral-rich, and chemically reducing, protected from surface UV and volcanic surface instability. Rich in H₂, CO₂, sulfides, iron, nickel, and other transition metals. (established — general characterization of vent environments)
- Deep-sea hydrothermal vents are a leading candidate environment for the origin of chemolithoautotrophic life. (plausible — one of several origin-of-life models, not a settled consensus)

## Organism

*General facts about LUCA and flagella/archaella evolving after it live in `../grimoire/domains-of-life/luca.md` and `../grimoire/domains-of-life/bacteria-and-archaea.md` — see those files rather than duplicating here.*

- The organism is sessile — fixed/attached to a rock surface at the vent mouth, not motile — consistent with many early chemolithoautotrophs being surface-attached (biofilms, mats on mineral surfaces) rather than free-swimming, since vent chemistry concentrates energy at a fixed location and there's no need to travel to reach it. (plausible — ecological inference from vent models, not a proven universal rule; early life likely included a mix of lifestyles)
- It has no flagella, no motor, no propulsion structure of any kind. (plausible — consistent with flagella being a post-LUCA, lineage-specific innovation, per `../grimoire/domains-of-life/bacteria-and-archaea.md`)
- It reproduces by division (splitting into two), the general mechanism by which single-celled life multiplies. (established as a general fact of cellular life; not vent-specific)
- Narration frames the split as happening because "being two things is more stable than being one" once the organism is big enough. (speculative — a narrative simplification of binary fission's growth-then-division trigger, not a specific claim about a documented biochemical checkpoint)

## Mechanism

- The best-supported model for the earliest life's energy metabolism is **chemolithoautotrophy**: energy from inorganic redox chemistry (H₂, H₂S, Fe²⁺ as electron donors), carbon fixed from CO₂ — not from organic molecules like sugar. (plausible — converging view across multiple origin-of-life models; no single settled answer for the very first metabolism)
- Sugars were plausibly present in the early ocean in **low concentration**, from abiotic synthesis (e.g. formaldehyde chemistry) and/or meteoritic delivery (confirmed in situ on asteroid Bennu samples: ribose, glucose, and other sugars). (established presence is plausible; concentration and bioavailability in open seawater specifically is doubtful — sugars are chemically fragile and don't concentrate well outside localized settings)
- The reaction is local and surface-based — chemistry contacting the organism's surface directly, with no evidence for or need of any internal signal propagation across the organism at this stage. (speculative — this is a narrative simplification for pedagogical purposes, not a specific claim about a documented biochemical pathway)

## Math model

- This organism's behavior is modeled mathematically as **dissolved-substrate Michaelis–Menten kinetics**, simplified to `output ≈ input / (constant + input)`. The real formula is `rate = Vmax·[S] / (Km + [S])` — [S] is the local concentration of a dissolved electron donor (H₂, H₂S, Fe²⁺) at the cell surface, Vmax is the reaction's ceiling rate, and Km is the concentration at which the reaction runs at half that ceiling. The simplified version drops Vmax and Km as named, separately-justified constants and folds them into one generic "constant" — the chapter doesn't need their specific enzymatic meaning, only the general shape they produce (rises, then flattens). This is chosen over a plain proportional model (`output ≈ rate·input`) because the organism has a finite number of enzyme copies — each one takes time to bind, process, and release a molecule before grabbing the next, so past some input level, adding more substrate stops increasing output. The proportional model has no such ceiling and quietly ignores that limit. The two curves compared:

  ```
  output ≈ rate·input (no ceiling)          output ≈ input / (constant + input) (saturates)
    |                              .           |                  . . . . . . . .   ← ceiling
    |                          .                |              .
    |                      .                    |           .
    |                  .                        |         .
    |              .                            |        .
    |          .                                |      .
    |      .                                    |    .
    |  .                                        |  .
    +---------------------------- input          +---------------------------- input
  ```

  One input, one saturating curve, straight to output — no summation, no threshold, no memory. This is deliberately the mathematical floor of the story: ch1 adds a weighted sum over multiple receptors plus a threshold switch, a genuine increase in structure over this single-curve behavior. (plausible pedagogical simplification — Michaelis–Menten is an established model for single-substrate enzyme kinetics in general, but is not documented specifically as a whole-cell description of a hypothetical LUCA-like organism's metabolism, which in reality involves a multi-enzyme pathway, not one isolated reaction)

## Open questions

- No specific organism/species is being named or claimed as historically exact — this chapter portrays a plausible generic early chemolithoautotroph, not a documented specific lineage. Needs an explicit framing decision: state this generically, or pick a defensible modern analog (e.g. a vent-dwelling archaeon) to ground the visual.
- Narration currently labels the opening pre-ocean/bombardment period "the Archean," but per `../grimoire/geologic-time/hadean-eon.md`/`../grimoire/geologic-time/archean-eon.md` that period is conventionally the **Hadean** eon — the Archean starts later, after oceans exist. Needs a decision: correct the name to Hadean, or keep "Archean" as a deliberate simplification (and if so, note why).

## Framing notes

- This chapter is set before any free-swimming, chemotaxis-driven organism, at a deep-sea hydrothermal vent rather than a shallow sunlit ocean. (story-ordering decision, not a checkable fact)
- This organism is **LUCA-like, not LUCA itself** — it shares LUCA's best-supported traits (anaerobic chemolithoautotroph, H₂/H₂S-driven, vent-dwelling, sessile, dividing by fission) but the chapter does not claim it *is* LUCA. LUCA's exact identity and traits are a reconstruction from comparative genomics, not direct observation, and remain contested — narration should not name-drop "LUCA" or assert this organism's timing relative to LUCA more precisely than the vague framing below.
- Exact timing (how early after LUCA, or before it) is unresolved in the literature and should stay vague in narration ("very early," not a specific number of years) unless a firmer date is found.
- Bacteria and Archaea are generally understood to descend from a shared common ancestor (LUCA), consistent with this organism being LUCA-like rather than a claimed member of either domain — though the exact rooting/order of the earliest splits in the tree of life remains actively debated as of 2024–2025 research, not settled fact. (plausible) The story picks up this fork in ch1 by following the Bacteria branch specifically and not narrating the Archaea branch; see `ch1-the-world-before-learning.md § Framing notes`.
- LUCA's fork is not limited to Bacteria and Archaea — the third domain, **Eukaryotes** (which includes every animal appearing from ch2 onward), plausibly arose later and from *within* Archaea specifically, via a symbiotic merger with a bacterium that became the mitochondrion — not as a third parallel branch splitting directly off LUCA alongside Bacteria and Archaea. See `ch2.1-when-many-cells-move-as-one.md § Early multicellularity` for how this connects to the animals the story follows from ch2 on. (plausible — a leading, well-supported model, still refined in its specifics)

