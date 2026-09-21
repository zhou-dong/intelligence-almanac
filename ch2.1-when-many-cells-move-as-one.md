# Facts — When Many Cells Move as One (Chapter 2.1)

*This file holds facts specific to this chapter. This is sub-chapter 2.1 of Chapter 2 — same period (Ediacaran) and same organism (a generic early bilaterian, not a specific named species) as sub-chapter 2.2 (`ch2.2-when-weights-learn.md`), split out only to keep each file a manageable length. 2.1 covers structure/convergence (fixed weights); 2.2 covers weights actually changing from experience.*

## Overview

This chapter opens after the Cryogenian "Snowball Earth" glaciations, in the Ediacaran (imprecisely captioned in the script as "600 million years ago, end of the Proterozoic" — that's actually mid-Ediacaran, not the Proterozoic boundary). Multiple multicellular lineages have arisen independently by now — sponges, cnidarians, and bilaterians — and the chapter follows a generic early bilaterian animal, based on real Ediacaran bilaterian body fossils: tiny (grain-of-rice sized), worm-like, bilaterally symmetric, with a distinct front/back axis and, inferred from body form plus matching burrow traces, a through-gut with a mouth and anus. The corrected framing (per the script's own flagged errata) is that tunable chemical synapses already exist earlier, in cnidarians' nerve nets — so that's not new here. What early bilaterians plausibly introduce is **centralization**: a primitive ganglion that gathers sensory signals from across the whole body into one place, sums them with weights and a bias, and produces a single output — the chapter's biology-first analogy to Rosenblatt's perceptron. Internal-state signals like hunger or arousal plausibly feed into that same convergence point alongside external senses. This is the story's first appearance of *one place where many signals become one decision* — a real structural leap from ch1's single fixed sensor-to-motor loop, even though the underlying tunable-junction idea (the synapse) isn't new. One caveat runs through all of this: fossils of this kind directly show body shape and burrowing behavior, not a nervous system — any claim about a ganglion is an inference from living simple bilaterians, not something the fossils themselves preserve. 

In short: bilaterians appear, and the chapter frames their (inferred) ganglion as perceptron-like structure — many inputs, weighted, summed, thresholded. But the weights are fixed, set by development/evolution, not adjustable within an individual's lifetime. No learning yet.

> **Status note:** this chapter's own script (`scripts/ch2-when-many-cells-move-as-one.md`) contains an unresolved `⚠️ UNRESOLVED` block (as of 2026-07-31) flagging that §1.1 and §1.2 of the current draft make claims that do not survive scrutiny. This facts file records the **corrected** framing below — Part 1/Part 2 of the script as currently written still needs a rewrite to match it. See "Open questions" for the specific sections affected.

## Setting — Earth history

- The Ediacaran period follows a series of severe glaciations ("Snowball Earth" events, the Cryogenian glaciations) during which much or all of Earth was covered in ice, then thawed. (established)
- Atmospheric oxygen built up gradually over billions of years, produced by bacterial (cyanobacterial) photosynthesis, prior to the Ediacaran. (established)
- The script's caption dates this chapter's opening to "600 million years ago, end of the Proterozoic." This is **imprecise**: the Proterozoic eon actually ends at ~538.8 Mya (its final period, the Ediacaran, runs roughly 635–538.8 Mya), so 600 Mya falls within the Ediacaran/late Proterozoic, not at its boundary. (established — dating correction; the ICS chronostratigraphic chart is the reference)

## Early multicellularity — one shared origin, then divergence

- **Correction:** sponges, cnidarians, and bilaterians did **not** each independently invent multicellularity. Animal multicellularity is understood to have arisen **once**, from a single common multicellular ancestor at the base of Metazoa (all animals) — that lineage then split, with these three groups diverging from each other afterward, not climbing from single cells to multicellular bodies in parallel. (established — one shared origin for animal multicellularity; the exact branching *order*, e.g. whether sponges or ctenophores split off first, remains an active, unresolved debate)
- Multicellularity as a broader phenomenon **has** evolved independently multiple times — but across separate kingdoms of life (animals, plants, fungi, and various algae each developed it separately), not among sponges/cnidarians/bilaterians specifically, which are one nested family tree. (established at this general level)
- All animals, including sponges, cnidarians, and bilaterians, are **eukaryotes** — a domain of life plausibly arising later than, and from within, Archaea, via a symbiotic merger with a bacterium (the ancestor of mitochondria); see `ch0-first-thing-alive.md § Framing notes` for how this connects back to LUCA's Bacteria/Archaea fork. (plausible — a leading, well-supported model for eukaryotic origin, still refined in details, not a settled single account of every step)
- Cnidarian descendants alive today include corals, sea anemones, and jellyfish. (established)

## The chapter's early bilaterian — body plan and behavior

- Real fossil bilaterians from the Ediacaran (e.g. from South Australia, dated to more than 555 million years ago) are widely interpreted as among the earliest known bilaterians; this chapter's organism is a generic stand-in of that kind, not a specific named species. (established — that such fossils exist and are dated this way; the chapter's organism itself is a generic composite, not a documented individual species)
- Body plan: very small (grain-of-rice sized, roughly a few millimeters long), elongated and worm-like, with clear bilateral (left-right) symmetry and a distinct head-to-tail axis. (established, from the body fossils themselves)
- A through-gut with two openings (mouth and anus) is the leading interpretation, but this is an **inference** from combining the body fossil's shape with matching burrow trace fossils in the same rock layers — the fossil does not preserve a complete, directly visible digestive tract. (plausible — a well-supported inference from combined body-fossil and trace-fossil evidence, not a directly observed organ)
- The burrow traces found alongside the body fossils show deliberate, forward-moving, sediment-reworking behavior consistent with active foraging — this is real, direct evidence of behavior (movement and feeding), independent of any claim about internal anatomy or nervous system. (established — the trace fossils themselves are the primary evidence)
- **No nervous system is directly preserved in fossils of this kind.** Any claim that it had a nervous system, let alone a specific ganglion structure, is an inference based on it being a bilaterian animal with directional, apparently purposeful movement — drawn by analogy to living simple bilaterians (e.g., acoels, flatworms) — not something the fossil itself shows. (speculative, relative to the fossil evidence itself — though a reasonable inference given its bilaterian body plan and behavior)

## Cnidarian ("radiatan") nervous system — corrected framing

*This section supersedes the framing in the script's current §1.1, which the script's own unresolved note flags as incorrect.*

- Nerve cells (neurons) appear earlier than bilaterians, in the cnidarian lineage. Cnidarians possess a **nerve net**: neurons distributed through the body with no central integration point. Stimulation at one location propagates outward through the net; there is no single site where signals from the whole body converge into one output. (established — high confidence per the script's own fact-check note)
- Cnidarians already have real chemical synapses between neurons, with variable transmission strength between different synapses. (established — high confidence per the script's own fact-check note)
- Consequence: the *tunable synapse* (a weight sitting in a connection, adjustable independently of the sensor) predates bilaterians and is not a bilaterian innovation. What bilaterians plausibly add is **centralization** — a specific place where signals from across the body converge into one decision — not the synapse itself. (established, given the above)

## Signal propagation — chemistry vs. wiring (used as narrative device)

- Diffusion-based (chemical) signaling time scales with the square of the distance traveled — a well-established physics fact (diffusion times generally scale as distance²/diffusivity). (established as a general physical principle)
- The script uses this to argue that at a body scale roughly 1000× a bacterium's, diffusion-only signaling becomes impractical (minutes-to-hours to cross a body), motivating wired (synaptic/electrical) signaling for larger, coordinated bodies. (plausible as a narrative/order-of-magnitude argument; the specific "~1000×" scale factor and resulting time estimates are illustrative, not sourced figures, and should not be presented as precise)

## Nervous cluster (ganglion) and the perceptron mapping

- A primitive ganglion — a small cluster of neurons receiving sensory input from across the body and sending motor output to muscles — is a real, established category of early nervous system organization in simple living bilaterians (e.g., flatworms). (established as a general biological structure — see the exception bullet below for a caveat on which bilaterians this applies to)
- Attributing such a ganglion specifically to this chapter's organism is **not directly supported by fossils of this kind** (per `§ The chapter's early bilaterian`) — it is an extrapolation from bilaterian body plan and behavior, by analogy to living simple bilaterians that do have ganglia. The chapter should frame this as "animals of this general kind plausibly had," not as a documented fact about any specific named species. (speculative extrapolation, not established for any single species)
- The chapter maps this (inferred) ganglion onto a perceptron (multiple weighted inputs, summed, plus a bias, producing a binary output) as a pedagogical analogy — biology first, math named second. This is a teaching framing, not a claim that early bilaterian ganglia are historically/literally identical to Rosenblatt's model. This chapter's organism itself is a generic stand-in, not a specific named fossil species. (plausible as a teaching model, explicitly flagged as a simplification in the script itself: "the real cluster isn't a single perceptron... it is a small network of them")
- **Structure vs. training — don't conflate these:** having the convergence structure (a ganglion) is not the same as being able to train it with Rosenblatt's error-driven rule. No bilaterian, including the best-documented living case, has been shown to implement literal error/target comparison — real documented plasticity (e.g. associative learning in *Aplysia*, per `ch2.2-when-weights-learn.md`) is mechanistically simpler than that. So "has the structure" and "trains like a perceptron" are separate claims with different evidence behind them. (established distinction between the structure and the specific learning rule)
- **Exception to "bilaterians are centralized":** not every bilaterian has a clearly centralized nervous system. Xenacoelomorpha (acoels and relatives, among the earliest-branching bilaterian lineages) include species with a more diffuse, net-like nervous system, closer to cnidarians than to a single ganglion. Whether centralization was already present in the bilaterian ancestor and lost here, or evolved more than once independently, is unresolved. (plausible/contested — a real exception, not a settled counter-rule)

## Math model

- The inferred ganglion is modeled with the **same formula as ch1's**: `signal ≈ Σ(wᵢ · xᵢ) + bias`, then `motor state ≈ threshold(signal)` (`ch1-the-world-before-learning.md § Math model`). Mathematically this is not a new equation — it's the same weighted-sum-plus-bias-plus-threshold shape recurring at a new physical scale, and the chapter should say so rather than presenting it as a fresh invention.
- What changes is what each `xᵢ` and `wᵢ` physically *are*. In ch1, the "many inputs" are receptor types on **one cell**, combined implicitly inside that cell via a single shared diffusible chemical (CheY-P), with weights fixed by gene-expression copy-numbers. In ch2, the inputs are **separate sensory neurons scattered across a whole multicellular body**, wired through discrete, individually tunable chemical synapses into one ganglion — a real multicellular convergence point, not one cell's internal chemistry. `xᵢ` can now include internal-state signals (hunger, arousal) alongside external senses, feeding the same convergence point.
- This tunability is **not new at this stage** — cnidarian nerve nets already have variable-strength synapses (`§ Cnidarian ("radiatan") nervous system`) — and nothing at this stage adjusts those weights based on outcome; there is no training/learning process yet. What is new is the **convergence**: for the first time, many separately-wired, individually-tunable junctions all feed into one place, producing one shared decision, rather than each sensor driving behavior locally or the whole net just propagating a stimulus outward. (plausible pedagogical simplification — the ganglion-as-perceptron mapping is a teaching framing per `§ Nervous cluster`, not a claim that early bilaterian ganglia perform this exact arithmetic, and the ganglion itself is an inference rather than a documented feature of any specific fossil species)

## Internal state signals (hunger, arousal)

- The claim that internal-state signaling (e.g., hunger signals from a gut, body-wide arousal under threat) co-evolved alongside nervous system integration in early bilaterians is a reasonable evolutionary inference but is stated flatly in the script with no citation. (plausible, not verified against a specific source)

## History — Rosenblatt and the perceptron

- Frank Rosenblatt is credited with formulating the perceptron and built a hardware implementation (the Mark I Perceptron) capable of learning, in the late 1950s. (established, widely documented)
- The script's specific date, "1958," and the quote attributed to Rosenblatt ("the simplest possible model of a neuron") are stated without citation — the underlying history is well documented, but this exact date and quote should be checked against Rosenblatt's original publications/reports before being treated as precisely sourced. (needs verification — established in broad strokes, unverified in exact wording/date)

## Framing notes

- This chapter's organism's foraging (moving toward food, evidenced directly by burrow traces of this kind) and any escape/withdrawal behavior are plausibly still **fixed reflex arcs** at this stage — the same fundamental mechanism as ch1's chemotaxis (a fixed weighted sum, thresholded into a motor output), just now converged through a (inferred) ganglion rather than driven by one cell's receptor cluster. The weights producing such behaviors would be set by development/gene expression, shaped by natural selection *across generations*, not adjusted by any individual organism's own experience within its lifetime. A behavior can look adaptive and goal-directed from the outside while still being entirely fixed on the inside — evolution did the "learning," not the individual. (plausible — consistent with reflex-circuit models of simple bilaterian behavior; not a claim that this chapter's organism specifically lacks any capacity for individual learning, just that none is needed to explain foraging/escape at this stage)
- Genuine individual-lifetime learning about food and danger — associating a specific stimulus with an outcome and changing behavior because of it (classical/operant conditioning) — is documented in some invertebrates (e.g., Aplysia, various insects), but requires outcome-comparing machinery closer to ch2.2's error-driven perceptron rule (`ch2.2-when-weights-learn.md § The perceptron learning rule`) than to anything in this chapter. Attributing that capability to this chapter's organism specifically would be a stronger, less defensible claim than the fixed-reflex framing above. (plausible caution against overclaiming; the perceptron rule itself is established, per ch2.2)
- **Eukaryotes arise from a merger of two LUCA-descended branches, not a straight chain through one domain.** The eukaryotic host cell itself (its core lineage, genetics, ribosomes) is understood to descend from *within* Archaea, closely related to a specific archaeal group (Asgard archaea) — not from Bacteria. Separately, at some point an archaeal host cell merged with a bacterium, which became the mitochondrion — a symbiotic partner living inside the eukaryotic cell, not the lineage the eukaryotic cell itself descends from. So the correct picture is `LUCA → Archaea (host lineage) → Eukaryotes`, with a bacterial lineage folded in afterward via endosymbiosis — not `LUCA → Bacteria → Eukaryotes`, and not a single linear chain through either domain alone. (plausible — a leading, well-supported model for eukaryotic origin, still refined in its specifics; see `ch0-first-thing-alive.md § Framing notes`)

  **Simple:**

  ```
  LUCA
   ├── Bacteria ──────────────────────┐
   │                                   (one bacterial lineage engulfed/merged in
   │                                    → becomes the mitochondrion)
   └── Archaea (host lineage) ──────── Eukaryotes
  ```

  **Full (annotated — where learning does and doesn't appear):**

  ```
  LUCA                                    ← ch0's organism: no nervous system,
   │                                        no learning (single-cell chemistry only)
   ├── Bacteria ──────────────────────┐   ← ch1's organism lives here: adapts
   │                                   │     (methylation re-zeroing) but this is
   │                                   │     NOT learning — resets toward its own
   │                                   │     history, never toward an outcome
   │                                   (one bacterial lineage engulfed/merged in
   │                                    → becomes the mitochondrion, not the
   │                                    host lineage itself)
   └── Archaea (host lineage) ──────── Eukaryotes  ← ch2's organisms live here;
                                                        see the animal-branching tree
                                                        below for where learning
                                                        first appears (cnidarians)
  ```

- **Branching order among animal lineages is a tree, not a ladder.** Sponges, cnidarians, and bilaterians are not sequential steps where one evolves into the next — each split leaves two sister lineages, only one of which keeps splitting further. The traditional (though actively disputed) view: the early animal ancestor's lineage split off sponges first, then the remaining lineage split off cnidarians, leaving bilaterians as the last-splitting group — meaning sponges and cnidarians are bilaterians' cousins, still alive today, not ancestors bilaterians "passed through." A competing hypothesis places ctenophores (comb jellies) as the first branch instead of sponges; this remains unresolved. (plausible — branching order specifically is an active, unresolved debate; the tree-not-ladder structure itself is established)

  **Simple:**

  ```
  Eukaryotes
       │
  early animal ancestor
       │
       ├── Sponges (branch off first — disputed; ctenophores are a competing "first branch")
       │
       └── (remaining lineage)
              │
              ├── Cnidarians (branch off next)
              │
              └── Bilaterians (last-splitting group)
  ```

  **Full (annotated — where learning does and doesn't appear):**

  ```
  Eukaryotes                                  ← domain-wide; most of this domain
       │                                        (yeast, amoebas, algae, plants, fungi)
  early animal ancestor                         has no nervous system and no
       │                                        documented capacity to learn
       ├── Sponges (branch off first — disputed;      no neurons/synapses at all —
       │            ctenophores are a competing        "can it learn" doesn't apply
       │            "first branch")
       │
       └── (remaining lineage)
              │
              ├── Cnidarians (branch off next)   ← FIRST organism in this tree that
              │                                     can learn: has synapses, and
              │                                     habituation (experience-based
              │                                     synaptic weakening) is documented
              │                                     here — no convergence point needed
              │
              └── Bilaterians (last-splitting group)  ← adds centralization (ganglion),
                                                          NOT learning itself — plasticity
                                                          already existed pre-bilaterian
  ```
- **Cnidarians are the earliest-branching lineage where synapse-weight-updating-from-experience is documented, because they're the earliest-branching lineage with neurons at all.** Per the branching tree above, sponges split off before cnidarians — and sponges have no neurons or synapses in the first place, so the question of experience-based weight change doesn't apply to them; there's nothing there to update. Cnidarians are the first branch in this tree that has synapses, and habituation (a synapse weakening its response purely from the animal's own repeated stimulation, no target or comparison involved) is documented in them. So the honest claim is "at least as old as the cnidarian lineage" — a relative/structural claim about where in the tree this capability first appears — not a claim datable to any specific era, since synaptic biochemistry leaves no fossil trace. (established for cnidarians specifically; the "earliest lineage where this is even possible" framing follows from the tree structure above, not a separate documented fact)
  - **Mechanistic depth — how habituation is thought to work here:** the leading candidate mechanism is **synaptic depression** — repeated stimulation reduces transmitter release or postsynaptic sensitivity at the same synapse (a *homosynaptic* effect, confined to the stimulated pathway rather than the whole network). Cnidarian nervous systems use both classical small-molecule transmitters (glutamate, GABA, serotonin, catecholamines) and, especially prominently, neuropeptides — so the transmitter identity involved likely varies by species and circuit. (plausible — synaptic depression is the general mechanism proposed for habituation across many animal groups, and cnidarians are known to have the relevant transmitter machinery, but the specific synapse-level mechanism has **not** been dissected in cnidarians with the same rigor as in the comparison case below)
  - **Contrast with *Aplysia* (ch2.2):** in *Aplysia*'s gill-withdrawal habituation, Kandel's group traced the mechanism to a *specific*, well-characterized cellular event — reduced calcium influx at the presynaptic sensory-neuron terminal, causing less neurotransmitter release onto the motor neuron. That is genuinely established, at the single-synapse level, for that one organism. No cnidarian study has pinned down an equivalently specific mechanism — so "cnidarians show habituation" is established, but "cnidarian habituation works via reduced presynaptic calcium influx" would be borrowing *Aplysia*'s mechanism by analogy, not a documented cnidarian-specific finding. Keep these two confidence levels distinct if this goes into narration.
- **Convergence and experience-based plasticity are independent capabilities, and plasticity is the older of the two.** A perceptron-style structure (this chapter's ganglion) is about *wiring* — gathering many inputs into one place before producing an output. Learning-from-experience is about a *single synapse* changing its own strength based on its own recent activity (e.g., habituation), which needs no convergence point at all: cnidarian nerve nets have no central ganglion anywhere, yet already show documented experience-based synaptic plasticity (`§ Cnidarian ("radiatan") nervous system`). So the historical order is plausibly the reverse of what the ganglion-as-perceptron framing might suggest — tunable, experience-modifiable synapses came first (pre-bilaterian), and centralization (this chapter's ganglion) arrived later, initially riding on fixed weights rather than introducing plasticity itself. (plausible — a structural inference from the cnidarian/bilaterian evidence already cited in this file, not a new documented fact)

## Open questions — sections needing a rewrite to match this file

- **Flag 1 (script §1.1):** framing an early bilaterian's lineage as "the first to evolve a nervous cluster" is incorrect as written — nerve nets (without centralization) predate bilaterians in the cnidarian lineage. Needs retitling/reframing around *centralization*, not *innervation*, as the bilaterian innovation.
- **Flag 2 (script §1.2):** "the weight moves out of the sensor" as a bilaterian invention is not safe as written — cnidarians already have tunable synapses. The chapter's territory narrows to: convergence (a place where dials are read *together*) and internal signals as inputs — not the existence of the tunable junction itself.
- **Flag 3:** the script must not present the ganglion, perceptron mapping, or internal-state-signal claims as documented facts about this chapter's generic early bilaterian itself — fossil evidence of this kind covers body plan and burrowing behavior only. These claims should be framed as "plausible for animals of this general kind," drawing on living simple bilaterians, not asserted specifically for any one species.
- These corrections do not affect §1.3 (internal signals) or the Ch0→Ch1 bridge about the bacterium's weight being welded to its detector — those comparisons are bacterium-vs-bilaterian and don't route through the cnidarian.
