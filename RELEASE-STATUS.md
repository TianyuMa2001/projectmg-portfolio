# Release verification - September 2026

Windows x64 player built successfully with Unity 6000.3.8f1. All four automated first-level modes reached Level 2 on accepted seed 5800.

| Mode | Seed | Steps | Engine seconds | HP after transition | Result |
| --- | --- | --- | --- | --- | --- |
| efficient | 5800 | 73 | 8.75 | 100 | level-cleared |
| fair | 5800 | 177 | 21.28 | 100 | level-cleared |
| omniscient | 5800 | 59 | 7.25 | 100 | level-cleared |
| traversal | 5800 | 157 | 18.89 | 100 | level-cleared |

These are single-run automation observations, not player performance benchmarks or evidence of survival improvement. HP after transition includes +10 HP healing. Headless modes cannot establish visual quality. The rendered check is separately recorded below.

Independent original-code checks: two-route A* (17 vs 29 steps; 7 vs 0 danger-zone tiles), chest threshold (64% accepted / 65% rejected), hidden-intermediate route gate and five PlayerController movement checks passed.

Pending: independent clean Windows machine, manual input/feel, formal external playtest, all 15 levels, historical before/after recordings.

Rendered check: the final Windows build ran with Direct3D 11 and reached Level 2. An explicit URP camera render produced a nonblank player/fog image that was visually inspected. Camera capture excludes screen-overlay HUD, and does not verify manual input.

External GitHub/commit HTTP checks could not complete because this machine could not resolve github.com; the bundled code/evidence remains available without GitHub access.
