# WL4 Public Validation

Public evidence and reproducibility surface for WL4 robotics/path-planning validation.

## IP boundary

The WL4 core implementation, selector logic, private heuristics, tuning history, and proprietary know-how are intentionally **not** published in this repository. This repository is limited to public validation workflows, public benchmark references, evidence manifests, and result artifacts that can be disclosed without exposing the private WL4 engine.

## Current scope

- GitHub-hosted runner availability checks on a public repository.
- Public MotionBenchMaker/VAMP validation scaffolding.
- Public STEP/CAD provenance and derived proxy evidence.
- Reproducible result manifests and hashes.

## Claim boundary

Public validation here does not by itself establish certified safety, physical robot latency, or exact B-Rep/mesh workspace collision checking. Where CAD-derived joint-space proxies are used, that limitation is stated explicitly.

## Private core

The commercial WL4 engine remains in a separate private repository and is not mirrored here.
