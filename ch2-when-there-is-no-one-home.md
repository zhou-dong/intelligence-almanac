# Facts — When There Is No One Home (Chapter 2)

*This file holds facts specific to this chapter.*

## Overview

This chapter follows a generic sponge, in the Ediacaran, as the first branch off the early animal lineage (disputed vs. ctenophores as the true first branch — see `ch4.1-when-many-cells-move-as-one.md § Branching order among animal lineages`). The chapter is a deliberate **contrast**, not a learning story: sponges have no neurons and no synapses at all, so there is no signal-weighting, no convergence point, and nothing that fits a "learning" narrative. What they do have is a real, non-neural, whole-body coordination mechanism — slow signals (e.g. calcium waves) propagating through sheets of epithelial-like cells — and a genome that already carries genes homologous to components later used to build neurons and synapses, without ever assembling them into an actual nervous system. The point of this chapter is structural: it establishes the floor (no computation substrate for anything perceptron-like) that chapter 3 (cnidarians, real synapses, no centralization) and chapter 4 (bilaterians, centralization) build on in turn.

## Body plan and physiology

- Sponges (phylum Porifera) are sessile, filter-feeding animals with a body organized around water channels — pores and canals draw water in, and specialized flagellated cells (choanocytes) drive water flow and capture food particles. (established)
- Sponges have **no neurons and no synapses of any kind** — no nerve cells, no nerve net, nothing structurally analogous to what cnidarians have. This is not a simplification; it is the standard, well-supported characterization of the phylum. (established)
- Sponges do have several differentiated cell types (choanocytes, epithelial-like pinacocytes, contractile myocyte-like cells in some species) — so "no neurons" does not mean "no specialized cells," just that none of those cell types are neurons or form synapses. (established)

## Coordination without neurons

- Sponges exhibit whole-body behaviors — most notably a slow, whole-body contraction response ("sneezing," documented in some species) — without any neurons to coordinate it. (established)
- The leading proposed mechanism for this coordination is **calcium-wave signaling**: a rise in intracellular calcium in one region of the epithelial-like cell sheet propagates to neighboring cells, cell-to-cell, without any dedicated wiring or synaptic junctions. This is a generic, slow, non-directional form of signaling — closer to a ripple spreading through a sheet than a routed message. (plausible — calcium-wave propagation is documented in sponge tissue; the full mechanistic picture, including which cell-to-cell junctions carry it, is still being worked out)
- Because there are no synapses, there is no equivalent of a "weight" anywhere in this system — nothing analogous to ch1's fixed receptor weights or ch4.1's tunable synaptic weights. A calcium wave either propagates or it doesn't; there is no documented graded, tunable strength parameter attached to any specific connection. (established, as an absence — this is the chapter's central contrast point)

## Genomic precursors — the parts exist before the machine

- Sponge genomes contain genes homologous to many components later used to build neurons and synapses in other animal lineages — e.g. genes related to synaptic scaffolding proteins and some neurotransmitter-pathway components. (established — this is a well-documented genomic finding)
- This does **not** mean sponges have "proto-neurons" or a hidden nervous system — homologous genes can be, and in sponges are, repurposed for other cellular functions (e.g. cell adhesion, secretion) rather than assembled into anything resembling a neuron or synapse. The genomic raw material predates its later neural use; that is a fact about deep evolutionary tinkering (co-option), not evidence of a sponge nervous system. (established distinction — a common point of narrative overclaim to avoid)

## Math model

- There is no formula for this chapter, and that absence is the point. Ch1 modeled a weighted sum over receptors (`signal ≈ Σ(wᵢ·xᵢ) + bias`, `ch1-the-world-before-learning.md § Math model`); ch4.1 modeled the same shape recurring at a ganglion. Sponges have no analogous structure to model — no discrete inputs being weighted and summed, because there are no synapses to carry a tunable weight and no convergence point to sum anything at. The calcium-wave mechanism above is a propagation phenomenon (closer to the diffusion-based signaling discussed in `ch4.1-when-many-cells-move-as-one.md § Signal propagation`), not a summation-and-threshold computation.
- Framed against the story's throughline: ch0 has one saturating curve, no summation, no weights, no memory. Sponges add multicellularity and a body-wide (if slow, generic) coordination signal, but still no weights, no summation, no memory of the perceptron-relevant kind. The first tunable, synapse-based weight appears in chapter 3 (cnidarians), and the first convergence point appears in chapter 4 (bilaterians). (plausible pedagogical framing — the ordering itself follows from the established facts above, not a new claim)

## Framing notes

- **This chapter is a contrast, not a learning story.** The organizing question is not "how do sponges learn" (they don't — there's no substrate for that question to apply to) but "what is missing that chapters 3 and 4 will add." Narration should resist any temptation to describe calcium-wave coordination as a primitive form of learning or memory — it is a real, documented coordination mechanism, but nothing about it stores information from past events or changes its own future behavior based on experience. (framing — flagged corrected 2026-09-21, after an earlier draft plan for this chapter proposed "how sponges learn" as the framing and that premise didn't survive fact-checking)
- Sponges are still alive today as a full, successful, diversified lineage — not an evolutionary "failure" or a rung on a ladder to bilaterians. The three-branch structure (sponges / cnidarians / bilaterians) in `ch4.1-when-many-cells-move-as-one.md § Branching order among animal lineages` is a tree, not a ladder; sponges are bilaterians' cousins, not their ancestors. (established, restating the tree-not-ladder point for this chapter specifically)
