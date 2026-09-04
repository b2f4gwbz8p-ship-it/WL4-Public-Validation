# WL4 Live Validation — recovery snapshot

Archived: 2026-09-04
Owner: William Smeets — Hellendoorn, The Netherlands
Original ChatGPT site slug: `wl4-live-validation`
Original project id: `appgprj_6a9aeaac1f1481919c6e83f63619d726`
Original recorded live URL: `https://wl4-live-validation.nh74dqfnvr.chatgpt.site`

## Purpose
Buyer-facing evidence portal for the WL4 Optimization Engine. The portal deliberately separates measured benchmark evidence from claims that still require independent industrial validation.

## Hero
**WL4 LIVE VALIDATION**

ROBOT MOTION PLANNING · VALIDATED EVIDENCE

**Inspect the evidence. Challenge the result.**

WL4 is a route recovery and post-optimization engine. This portal separates measured benchmark evidence from claims that still require independent industrial validation.

Created by William Smeets, Hellendoorn, The Netherlands.

## Proof-of-concept challenge
Interactive replay — NOT LIVE WL4 COMPUTE.

Controls represented in the recovered site:
- Robot: Panda · 7-DOF / UR5 · 6-DOF / Fetch · Mobile manipulator
- Scene difficulty: Standard obstruction / Narrow passage / Invalid-seed recovery
- Replay budget: 5.0 s
- Run challenge replay

Disclosure: this control replays a representative recorded outcome. It does not send a new problem to the protected WL4 engine.

## Benchmark explorer
Recorded evidence — not a live engine run.

Recovered headline evidence:
- V11 recovery: 777/780 (99.62%) valid recoveries versus 771/780 for informed native VAMP RRTC.
- Post-optimization: 1,318 improved direct cases, 44 equal and 0 degraded across 1,362 valid evaluations.
- Native OMPL Track-A: 24/24 strict-valid; PRM 20/24, RRTConnect 11/24, RRTstar 3/24.
- Raw run artifacts and provenance were produced through successful CI jobs.

## Claim integrity
### Demonstrated in scope
- High recovery validity in the V11 benchmark.
- Direct post-optimization with no measured degradation in the valid set.
- Strict-valid performance across native OMPL Track-A cases.
- Reproducible CI artifacts and provenance.

### Still requires buyer validation
- Universal superiority over every planner.
- Real-time sensor-to-actuator performance.
- Dynamic obstacles on physical hardware.
- Buyer-specific CAD savings and engineering hours.

## Next evidence gate
**Run a private industrial challenge**

A controlled buyer trial uses the same scene, constraints and compute budget. WL4 remains server-side; the buyer receives a traceable comparison report.

## Recovery / safety note
This file was created after the original site became difficult to locate/open. It is a durable textual recovery snapshot, not a claim that the original hosted site remains reachable. The proprietary WL4 core, private selector logic, heuristics and know-how are intentionally excluded from this public backup.
