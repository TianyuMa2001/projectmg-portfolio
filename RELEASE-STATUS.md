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

## Original-art correction — September 13, 2026

Restored all 278 raster files, including their original alpha transparency and sprite-sheet pixels. Grass RuleTile and player prefab were compared with GitHub baseline 6ed95c17226cbba26273d56ad8dab2eab1b4c662 and matched the local originals. Existing .meta GUIDs and sliced sprite IDs are retained.

The final original-art Windows player built successfully. A rendered Efficient (J) run completed Level 1 on seed 5800 with the same initial tile geometry as the earlier verification. Actual camera captures show the original ground, wall, player and item visuals. The full-map image temporarily disables only the visual fog renderer for the explanatory capture, then restores the renderer and camera; it does not reveal hidden tiles to the planner. Marker positions come from that camera's WorldToViewportPoint.

The owner reports the download function works. This does not establish a clean-machine launch test or a formal playtest. The original-art correction was independently rechecked in Efficient mode; the earlier four-mode results remain historical verification of the same gameplay code with substitute artwork.
