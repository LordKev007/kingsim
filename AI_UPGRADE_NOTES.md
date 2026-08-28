# AI upgrade notes — v0.5.0

The CPU upgrade was based on the curated `Kings_Grid_GOOD_Learned_CPU_Data_2026-08-27` package.

Key signals incorporated:

- Corrected MASTER policy weights (safety 1.75, kite 1.55, kill bonus 3.2, threat focus 1.35, pressure 1.05, etc.).
- Exact shared initiative tempo as a tactical input.
- Move → Action → remaining Move search as a core requirement.
- Corrected fighter results showing particularly strong tactical value from Lance and Spear, with Master extracting substantially more value from Sword and Spear than the weaker learner.
- Observed percentage of combat deaths before a unit's own initiative (Sword 13.3%, Spear 37.3%, Bow 66.1%, Lance 86.8%, Mage 97.2%, late support pieces ~100%).
- Selective rather than spammy Mage and Strategist use.
- Bow ammunition conservation.
- Better support survival and post-action retreat.
- Wall value based on cover/disruption instead of random placement.
- Draw avoidance through advantage-conversion pressure without deliberately suicidal play.

The package explicitly warned that the final corrected Learner validated worse than its starting point. Those final learner weights were therefore **not** used as the new CPU seed.
