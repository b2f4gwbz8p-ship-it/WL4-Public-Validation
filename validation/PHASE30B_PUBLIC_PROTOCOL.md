# WL4 Phase 30B — Public Validation Protocol

Status: preregistered public validation surface; WL4 core remains private.

## Purpose
Provide a public, reproducible evidence layer for Phase 30B without publishing WL4 implementation, selector logic, heuristics, tuning history, or proprietary know-how.

## Frozen evidence boundary
- Public CAD source: `cloudgripper/cloudgripper-robot`, `Arm/Arm_grip_link2.step`, branch `master`.
- STEP blob SHA: `098913499ad7d6c11855b1312ffd1379190ef691`.
- Derived AABB: 16.5 x 5.0 x 5.0 mm.
- Conservative bounding radius over longest dimension: `0.5*sqrt(16.5^2+5^2+5^2)/16.5`.
- Proxy scale fractions: 0.02 and 0.04 of nominal joint-space path span.
- Dynamic speeds: 0.10, 0.25, 0.50.
- Horizon: 1.0.
- Full-loop deadline: 10 ms.
- Robots: Panda, UR5, Fetch.
- MotionBenchMaker scenario: `bookshelf_tall`, up to 100 identities per robot.
- VAMP revision family: v0.6.4.
- No WL4 tuning after observing Phase30B CAD-proxy outcomes.

## Architecture
The public repository contains only public inputs, provenance, validation logic, result manifests/hashes, and public runner checks. The private WL4 implementation is not copied into this repository and must not be exposed through logs or artifacts.

A Phase30B result is not accepted merely because the public runner works. Acceptance requires externally inspectable result evidence produced by an execution of the frozen WL4 candidate, followed by public verification of provenance and result integrity.

## Required result fields
For each robot: exact problem identities, event count, successful recoveries, no-candidate count, static-invalid successes, swept-unsafe successes, exceptions, deadline-met count, and full-loop p50/p95/p99/max. The exact maximum must be retained even when it exceeds 10 ms.

## Acceptance gates
1. Exact public CAD provenance and AABB/proxy math are reproducible.
2. Frozen WL4 identity is cryptographically bound to the result package without publishing source.
3. Panda, UR5 and Fetch result packages exist and pass schema/integrity verification.
4. Zero static-invalid successful outputs.
5. Zero swept-unsafe successful outputs.
6. Exceptions are reported exactly; no silent filtering.
7. Deadline compliance is calculated from actual timing values, not a surrogate failure category.
8. Any deadline miss remains visible and prevents a blanket hard-real-time claim.

## Claim boundary
Phase30B uses a conservative CAD-derived bounding-sphere joint-space proxy because the current WL4 safety kernel is joint-space swept-sphere based. It is not exact B-Rep/mesh workspace collision checking, not physical sensor-to-actuator latency, not certified robot safety, and not confidential buyer CAD.

Permitted framing after successful execution: frozen WL4 was evaluated with a conservative joint-space collision proxy reproducibly derived from independently published STEP geometry, with exact safety and software-loop timing evidence.
