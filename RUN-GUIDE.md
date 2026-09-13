# ProjectMG - Portfolio Review Edition

Tianyu Ma - Technical Designer. C# / Unity team course project.

## Windows launch
Extract the entire Windows ZIP and run ProjectMG.exe. Keep ProjectMG_Data, MonoBleedingEdge and UnityPlayer.dll beside it. Windows x64; Unity Editor is not required. Original artwork has been restored with the portfolio owner's confirmed public display and redistribution permission. This is an unsigned mechanics review build.

## Goal and controls
Explore, collect the yellow key, then step onto the cyan exit to advance. A key is required. Chests heal 5 HP; purple Path terrain deals 10 damage per second. Clearing a level heals 10 HP and consumes the key. The team game contains 15 levels.

- WASD / arrows: move, including manual diagonals.
- T: start/pause two-phase traversal.
- G: start/pause Omniscient GoalAI.
- H: start/pause Fair GoalAI.
- J: start/pause Efficient GoalAI; recommended first demonstration.
- Hold Tab: expanded minimap.
- R: restart after final completion. Death restarts automatically.

Stop an automatic mode with its toggle before manual input. T can resume after key pickup while paused. Auto-navigation uses four directions. H/J gate normal paths and targets to discovered tiles but still read hidden-monster costs. T relaxes fog restrictions once the exit is revealed.

## Stable configuration
The isolated build uses randomSeed=false, initial Unity seed 5800, immediate generation and the team's existing Delaunay/Kruskal generator. Level 1 is 40 x 40. Retried generation can replace the seed; compare accepted seeds and initial geometry, not merely requested seed. Recorded modes all accepted seed 5800.

Optional validation launch: ProjectMG.exe --portfolio-output ABSOLUTE_DIRECTORY --portfolio-mode efficient (also fair, omniscient, traversal). Records an attempt and quits at completion, stop, death or 90 seconds. Normal launch does not automate the game.

## Source and evidence
Baseline: 6ed95c17226cbba26273d56ad8dab2eab1b4c662.
https://github.com/CS5800GroupHACHIMI/MapGeneration
The source/evidence ZIP contains project scripts, MIT notice, independent .NET checks, and recorded route JSON. It is not a complete Unity project. Open the GitHub project with Unity 6000.3.8f1 for the full original source. Original art remains copyrighted; the portfolio owner confirmed permission for this public review edition. To recreate this edition, prepare the isolated demo, run portfolio/work/restore_original_art.py after the legacy preparation script, then build with PortfolioBuild.Build. The legacy prepare_demo.py alone creates the superseded abstract edition. See RELEASE-STATUS.md for scope.

Independent check: from a full source checkout, run dotnet run --project portfolio/work/evidence/Evidence.csproj -- portfolio/deliverables/evidence. Its generator adapter uses System.Random, so it does not reproduce Unity's seed map. Its routing fixture uses fixed geometry.

No clean-machine test, formal participant study, manual-input session or complete 15-level campaign verification is claimed.
