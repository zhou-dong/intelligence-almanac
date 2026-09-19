# Facts — The World Before Learning

*This file holds facts specific to this chapter.*

## Overview

This chapter leaves the vent's stillness behind for a cell that swims and decides. This organism moves by "run and tumble" — its flagella bundle into a smooth propeller (run) or fling apart into a random reorientation (tumble), switching between the two based on a single internal chemical signal. Receptors packed together at one pole of the cell sense attractants and repellents, feeding a shared signaling pool that acts like a weighted sum: attractant lowers the signal, repellent raises it, and every receptor's influence depends on how many copies of it there are. When that pooled signal crosses a threshold, the motor snaps from mostly-running to mostly-tumbling — a switch, not a dial. Layered on top is a slower adaptation mechanism: methyl marks on the receptors drift over seconds to re-zero the signal back toward baseline, giving the cell a short chemical memory of its own recent stimulus — but one blind to whether tumbling or running actually helped. This adaptation works symmetrically in both directions: sustained food-seeking (attractant) stimulation and sustained danger-escape (repellent) stimulation each get re-zeroed by their own receptor channel, just via opposite-direction methylation changes, so the cell doesn't get stuck maximally responsive to either one. This is the story's first appearance of sensing-at-a-distance and a real decision loop, but it is still not learning: the adaptation always resets toward the cell's own history, never toward an outcome.

## Chemotaxis signaling — evolutionary origin

- The core Che signaling module (CheA/CheY/CheB-style two-component architecture) is **broadly conserved across Bacteria and Archaea**, suggesting an ancient origin for chemotactic *signaling* logic specifically. (established, per comparative genomics reviews)
- This conservation does **not** imply a single ancestral flagellum at LUCA — signaling and the motility structures it eventually couples to appear to have evolved on different timelines. (plausible)

## Run and tumble — the motor mechanism

- Run and tumble are mutually exclusive states of the flagellar motor: counterclockwise rotation bundles the flagella into a single coherent propeller (run); clockwise rotation flings the bundle apart (tumble). (established)
- At rest in uniform conditions, *E. coli* runs for roughly 1 s and tumbles for roughly 0.1 s, repeating continuously. (established — Berg & Brown 1972)
- The motor's response to intracellular signal level is steeply sigmoidal — effectively a threshold/switch, not a graded dimmer. (established — the steepness itself is well documented; see "unverified figures" below for the specific numeric threshold)

## Sensing and signal integration

- Receptors sit in a single dense cluster at the cell's pole, not scattered across the membrane; different receptor types (attractant-binding, repellent-binding) are packed side by side in that cluster. (established)
- The signaling enzyme (CheA in *E. coli*) exists in far fewer copies than there are receptors, and each copy is shared by several neighboring receptors of possibly mixed type — so opposing signals can meet at a single enzyme copy, not just in the shared downstream pool. (established, structurally — the two-stage "local opposition, then shared pool" framing is a pedagogical simplification of this structure, plausible as a teaching model)
- All enzyme copies feed the same diffusible signaling chemical (CheY-P) into the same cell interior; this shared pool is the only thing the flagellar motors can read — no motor has access to an individual receptor or enzyme copy. (established)
- CheY-P is continuously degraded by a dedicated enzyme (CheZ in *E. coli*), so its steady-state level tracks recent signal rather than accumulating indefinitely. (established)
- Attractant binding *lowers* CheA's output rate (less CheY-P produced); repellent binding *raises* it. (established)
- Receptors in the cluster are allosterically coupled to their neighbors — when one flips state, it biases nearby receptors (including unbound ones) toward the same state. This clustering is the mechanism generally credited with the pathway's high sensitivity (detecting changes far smaller than a single receptor's affinity would allow). (established as a mechanism; the specific gain/cluster-size figures below are unverified)
- Different receptor types are present in different copy numbers (e.g., typically more attractant receptors than repellent receptors of a given class), and this copy-number difference is what determines each signal type's relative influence on the shared pool. (established as a general principle; exact ratios for any given receptor pair are not verified here)
- The resting/baseline level of CheY-P (in the absence of added stimulus) is set by the unliganded receptor array holding the enzyme active — not by any intrinsic activity of the enzyme itself. Detached from receptors, CheA is nearly silent. (established)

## Adaptation — the memory mechanism

- Receptors carry methyl groups added by CheR and removed by CheB, which shift on a timescale of seconds and adjust each receptor's baseline signaling activity. (established)
- Adaptation is **bidirectional/symmetric**: it re-zeros the signal after sustained stimulation from *either* attractant (food-seeking) or repellent (danger-escape) binding, not just one direction. The methylation change runs opposite ways depending on which: attractant binding lowers receptor activity, so methylation *increases* to restore it; repellent binding raises activity, so methylation *decreases* to bring it back down. Either way, the goal is the same — reset toward the pre-stimulus baseline. (established)
- Adaptation is **receptor-type-specific**: sustained attractant stimulation adapts (re-zeros) only the attractant-sensing channel; it does not change the sensitivity of repellent-sensing receptors in the same cluster. (established — this is why the chapter's script explicitly avoids framing adaptation as "moving a single global bias")
- This methylation-based adaptation drives the stimulated receptor back toward its own resting signaling state, regardless of outcome — it responds only to the receptor's own recent input history, not to any measure of whether the cell's behavior "worked." (established as a mechanistic description; the framing "it never reaches outcome" is a direct, uncontested consequence of the pathway having no outcome-sensing component, not a separate claim needing its own citation)

## Math model

- This organism's behavior is modeled mathematically as a **weighted sum plus bias, followed by a threshold**: `signal ≈ Σ(wᵢ · xᵢ) + bias`, then `motor state ≈ threshold(signal)`. Each `xᵢ` is one receptor's binding state, each `wᵢ` its relative influence (set by how many copies of that receptor type exist and whether it's attractant- or repellent-binding — attractant weights push the signal down, repellent weights push it up), and `bias` is the resting/baseline level the unliganded receptor array holds the signaling enzyme at. `threshold(...)` is a steep sigmoid, not a smooth ramp — past a critical signal level the motor snaps from mostly-running to mostly-tumbling rather than sliding gradually between them.
- This is a genuine step up in structure over ch0's single-input, single-curve model (`ch0-first-thing-alive.md § Math model`): many inputs are combined into one number for the first time, that number can be pushed in *two directions* (excitatory vs. inhibitory), and the output is a hard switch rather than a saturating ceiling.
- Adaptation adds a slower **memory term** on top: the resting `bias` for each receptor type drifts, over seconds, toward whatever that channel's own recent input has been — so the formula's `bias` isn't a fixed constant but something the system continually re-centers based on its own history. Critically, it re-centers toward *recent input*, not toward any measure of outcome — there's no term in this model for "did running or tumbling just work."
- (plausible pedagogical simplification — the underlying biochemistry (shared signaling pool, copy-number-dependent influence, sigmoidal motor response, methylation-based re-centering) is established; "weighted sum," "bias," and "threshold" are narration-level framings of that biochemistry, not the field's own terminology for it)

## Figures needing verification before use in narration or captions

*Carried over from the script's own fact-check pass (compiled 2026-08-02). These are recalled/order-of-magnitude figures, not sourced here — prefer qualitative language ("a change too faint to notice") over the specific number until verified.*

- "~10% change in CheY-P level swings the motor from mostly-running to mostly-tumbling" — the qualitative steepness is established; this exact percentage is unverified.
- "A few thousand receptors" and "a few hundred CheA copies" per cluster — right order of magnitude, exact ratio unverified.
- "Roughly a dozen receptors act as a coupled unit" — cluster/team size is reported to vary with methylation state; this specific number is unverified.
- "Four seconds" of adaptation-based memory — the timescale is genuinely on the order of seconds; this specific figure is unverified.
- Overall pathway signal gain ("tens-fold") — commonly cited in the chemotaxis literature but unverified here.

## Framing notes

- This chapter's organism is not narratively claimed to be a direct descendant of ch0's vent organism, but its domain is now made explicit: this is the **Bacteria** branch. Both Bacteria and Archaea plausibly descend from ch0's LUCA-like ancestor (per `ch0-first-thing-alive.md § Framing notes`), and the story simply chooses to follow the Bacteria branch from here on, without narrating the Archaea branch — not a claim that Archaea are less important or came later. Flagella (Bacteria) and archaella (Archaea) are independently evolved, non-homologous rotary motility structures — neither inherited from LUCA — while the chemotaxis signaling module (Che genes) is separately conserved across both domains, so this organism's flagellar motor being "bolted onto" pre-existing signaling logic, in a later bacterial lineage, is more defensible than this specific ch0 organism growing a flagellum itself. The chapter break is left to signal that jump; the exact lineage between ch0 and ch1's organisms within Bacteria stays implicit and unstated in narration. (plausible — inference from flagellum/archaellum vs. Che-module evolutionary independence, not a documented single-lineage transition)
- Committing to the Bacteria branch resolves a mechanism-level detail: bacterial flagella produce run-and-tumble (a threshold switch into a randomizing tumble), while archaella (Archaea) produce run-reverse (switching rotation direction, not randomizing orientation) — the two are not narratively interchangeable. This chapter's run-and-tumble description is therefore consistent with its now-explicit domain. (established mechanistic distinction between the two motor types)
- The if/else framing (run vs. tumble as mutually exclusive branches) is faithful rather than decorative specifically because (a) the motor response is a genuine threshold/switch, and (b) run and tumble are mechanically exclusive states — not because biologists describe the pathway using "if/else" language themselves.
