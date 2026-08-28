# King's Grid Battle Practice Training Mode v0.5.0

Browser-based Human-vs-CPU Battle Practice for King's Grid, designed primarily for iPad landscape play.

## v0.5.0 — stronger CPU

This build upgrades **Mid** and **Master** using the curated corrected 500-battle AI study supplied for the project.

Important: the build does **not** copy the study's failed final Learner weights. It follows the package's recommendation to start from the corrected hand-designed MASTER policy and carry forward the validated tactical lessons.

### Mid

- Uses tactical move/action/move search rather than simple greedy movement.
- Values kills, initiative denial, safety, target importance and post-attack retreat.
- Improved Medic/revival positioning, selective Mage use, walls, Bread and Strategist use.
- Small amount of exploration remains so Mid is strong but not completely deterministic.

### Master

- Uses the corrected MASTER policy seed: high safety awareness, kill/tempo bonuses, threat focus, kiting, pressure, support value, selective Mage/Strategist thresholds.
- Searches **partial move → action → remaining move** lines.
- Uses Coach Bob's initiative-aware threat projection to judge whether the final square leaves a unit hanging before its next activation.
- Gives extra value to killing units before their initiative, informed by the corrected study's observed death-before-own-step rates.
- Improved Lance/Spear/Sword tactics, Bow ammunition discipline, Spear knockback board control, support retreat, wall placement and advantage conversion.
- Refuses ordinary attacks on Iron walls.
- Becomes more willing to convert an advantage instead of endlessly kiting as a battle drags on.

## Existing Training Mode features

- 10×10 board and locked Battle Practice rules
- Beginner / Mid / Master CPU
- Coach Bob live suggestions
- Human and CPU post-game reviews
- 1–100 review scores and key teaching moments
- Concede and stalemate controls
- 60-round cap
- iPad/touch-first interface

## GitHub Pages

Upload these files to the repository root, then publish the `main` branch from `/ (root)` in **Settings → Pages**.
