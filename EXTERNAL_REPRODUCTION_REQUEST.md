# WL4 Phase32 — External Independent Reproduction Request

Date issued: 2026-09-03
Owner/developer: William Smeets
Product: William Smeets WL4 Robotics Optimization & Recovery Engine

## Purpose
This request is the hand-off boundary from same-account isolated reproduction to a genuinely independent reproduction. A qualifying reproduction must be executed by a third party outside the developer's GitHub account/control environment. The third party must control its own compute environment and retain the original logs/results.

## What must remain fixed
- Scenario: `bookshelf_tall`.
- Robots: Panda, UR5, Fetch.
- First 100 official MotionBenchMaker problems per robot.
- VAMP v0.6.4 commit: `8fd768f9974a185a8aa2b4f370e595a8c3ca13cf`.
- Public STEP source Git blob: `098913499ad7d6c11855b1312ffd1379190ef691`.
- Frozen WL4 source identities supplied in the sealed reproduction manifest/package must verify before computation.
- No outcome-dependent tuning is permitted after results are observed.
- Registration must be reported exactly and may not be described as manufacturer/buyer industrial CAD registration unless it actually is one.

## Timing policies to report separately
1. Original evidence lane: <=10.0 ms full software loop.
2. Phase31H prospective lane: <=10.0 ms primary target, bounded >10 to <=15.0 ms stretch.

A result in the stretch lane must never be reported as a <=10 ms success.

## Required safety reporting
The reproducer must report at minimum:
- total events;
- accepted recoveries;
- no-candidate events;
- candidate mesh-collision events;
- mesh-rejected events;
- accepted mesh collisions;
- static-invalid accepted outputs;
- swept-unsafe accepted outputs;
- exceptions;
- deadline counts;
- full-loop min/median/p95/p99/max where available;
- exact source/STEP/VAMP hashes;
- runner OS/CPU/Python/dependency versions.

## Required evidence return
A qualifying external reproduction should return:
1. immutable raw JSON outputs;
2. complete execution logs;
3. SHA-256 digest for every returned artifact;
4. environment manifest;
5. signed statement identifying the reproducing person/organization and confirming that William Smeets did not tune code or acceptance gates after the third party observed outcomes;
6. PASS/FAIL against the preregistered gates, including deviations without reinterpretation.

## Independence rule
A run controlled solely by William Smeets or by repositories/runners under the same account/control boundary does **not** count as true external independent reproduction. A separate repository alone is insufficient. Independence requires a third party controlling the execution environment and preserving the evidence.

## Claim boundary
Successful reproduction would strengthen reproducibility evidence. It would not by itself establish certified functional safety, physical sensor-to-actuator latency, exact robot-link B-Rep validation, buyer-specific CAD registration, industrial deployment readiness, or measured economic ROI.

## Commercial sequence after successful external reproduction
External reproduction -> confidential buyer CAD/robot-cell case -> measured engineering/commissioning/downtime value -> acquisition/licensing evidence dossier.
