<!--
Copyright (c) 2026 JG Systems Consulting Ltd. - MIT License (see LICENSE).
SPDX-License-Identifier: MIT
-->

<h1 align="center">jgs-uk-defence-knowledge-packs</h1>

<p align="center">
  <img src="https://img.shields.io/badge/license-MIT%20(tooling)-blue" alt="License: MIT (tooling)">
  <img src="https://img.shields.io/badge/version-0.1.0-green" alt="Version 0.1.0">
</p>

<p align="center">
  <strong>One open reference catalogue of UK Defence safety-management knowledge
  packs for coding agents, with a single orchestrator that routes free-text
  questions to the right pack.</strong>
</p>

**Copyright (c) 2026 JG Systems Consulting Ltd. - MIT License (tooling); pack content under each source's own licence (see [NOTICE](NOTICE)).**

---

## What it is

This repo holds knowledge packs for the UK Defence safety domain: the JSP 815
Defence Safety Management System, its Safety Management System (SMS) framework
and 12 Elements, safety cases, assurance, and audit practice. Each pack is a
set of synthesized reference notes built from openly licensed sources (Open
Government Licence v3.0), packaged as an installable skill for coding agents.

This is not formal legal or regulatory advice, and it is not an official MOD
publication: it is reconstructed reference material, not a reproduction of the
sources. Further packs (Defence Standards and other JSPs) are forthcoming; the
jsp-815 pack is the first to land.

## Install

From the repo root:

```bash
python install.py --dry-run   # preview
python install.py             # install packs into your coding-agent skills directory
```

`install.sh` and `install.ps1` do the same on POSIX and Windows.

## Use

- **/ukdef** — the orchestrator. Type `/ukdef <question>` and it routes the
  question to the right pack in this catalogue.
- **/jsp-815** — the JSP 815 Defence Safety Management System pack: SMS
  framework, the 12 Elements, safety cases, assurance, and audit.

## Gates

Run all three from the repo root:

```bash
python tooling/validate_pack.py --all   # every pack matches docs/PACK-SPEC.md
python tooling/check_release.py         # release readiness: files, versions, leaks, links, index, headers
python tooling/test_ci_gate.py          # proves CI (.github/workflows/validate.yml) checks the same things
```

CI green is not release-ready: `check_release.py` is the pre-tag gate. It prints a
`RELEASE CHECK: PASS (v<version> @ <sha>)` receipt; run it before tagging and confirm
the sha matches the commit you tag. The repo is release-ready only when all three
gates exit 0 (see [docs/FLEET-CONVENTIONS.md](docs/FLEET-CONVENTIONS.md)).

## Licence

Two separable layers:

- **Tooling and scaffolding:** [MIT](LICENSE) (JG Systems Consulting Ltd.).
- **Pack content:** each pack carries its source's own licence, declared in
  `packs/<slug>/LICENSE` and `packs/<slug>/PACK.yaml`, independent of the repo's MIT
  licence. Attributions live in [NOTICE](NOTICE); the model is set out in
  [docs/LICENSING.md](docs/LICENSING.md).
