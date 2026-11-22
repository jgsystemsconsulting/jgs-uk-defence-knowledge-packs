<!--
Copyright (c) 2026 JG Systems Consulting Ltd.: MIT License (see LICENSE).
SPDX-License-Identifier: MIT
-->

# Changelog

All notable changes to this project are documented here. Format follows
[Keep a Changelog](https://keepachangelog.com/en/1.1.0/); versioning follows
[Semantic Versioning](https://semver.org/).

## [Unreleased]

## [0.3.0] - 2026-11-22

### Added

- jsp-376 content pack (JSP 376 Defence Acquisition Safety Policy; transplanted from SE).
- jsp-912 content pack (JSP 912; transplanted from SE).
- jsp-936 content pack (JSP 936 Dependable AI in Defence Part 1 Directive; transplanted from SE).
- Fleet advisory slug-duplication checker (`tooling/check_pack_slug_dupes.py`); advisory only, not wired into CI gates.

### Changed

- Catalogue now six live packs plus one signpost (iso-45001-signpost). Capability map notes count 72.

### Documented

- SE disposition: SE release v1.24.4 removes four slugs including jsp-815 (local annotated tag exists; not pushed at cut time).
- Drift window: consumers with both catalogues installed update SE to v1.24.4 so UK owns the moved slugs alone. Until SE v1.24.4 is pushed and consumed, both copies can coexist.
- Slug-duplication advisory currently reports UK four cleared once SE v1.24.4 lands; five sector collisions remain in SE (easa-rules, faa-8110-49, fda-med-device, nhtsa-vehicle, nrc-nuclear) and are SE-side work.

## [0.2.0] - 2026-11-22

### Added

- jsp-375 content pack (JSP 375 Management of Health and Safety in Defence; 10 chapters).
- jsp-816 content pack (JSP 816 Defence Environmental Management System; 11 chapters).
- iso-45001-signpost citation-only signpost (ISO 45001; no chapter body).
- Boundary note and PACK-SPEC neighbour rule for jsp-815 / ukdef scope and limits.
- patterns.md for jsp-815 technique patterns.

### Changed

- jsp-815 Annex G folded into chapter set (build.chapters now 11).

### Documented

- DEF-STAN 00-051 recorded exclusion (cover vet outcome; not landed as pack).

## [0.1.0]: 2026-09-24

### Added

- Initial public release: jsp-815 knowledge pack (JSP 815 Defence Safety Management System V1.3, Open Government Licence v3.0) and /ukdef orchestrator.
