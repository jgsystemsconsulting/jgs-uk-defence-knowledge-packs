# Capability to Knowledge-Pack Map

Working artifact mapping sector technical capabilities to the pack chapters that provide
reference depth for each capability. Empty-tree template seed: no content packs yet.

Rules of construction:
- Every chapter in every pack under `packs/<slug>/chapters/` is assigned to exactly one capability cluster (best fit).
- Signpost packs contain no chapters and are not mapped.
- Machine-readable version: `docs/capability-pack-map.json`.
- Machine-readable classification rules: `docs/classification-rules.json`.
- Changelog (v0.1.0): empty-tree template seed.

## Summary

| Cluster | Entries |
|---|---|
| 1. Safety Management Framework & Governance | 6 |
| 2. Risk & Operational Control | 4 |
| 3. Performance & Assurance | 2 |
| **Total** | **12** |

## 1. Safety Management Framework & Governance

| Pack | Chapter | Why it fits / one-line value |
|---|---|---|
| jsp-815 | ch01-defence-safety-jsp-map.md | Which JSP answers what: JSP 815 SMS, JSP 816 EMS, JSP 375, JSP 376, JSP 814, SofS Policy Statement, Safety Function Operating Model, DSA regulators, and duty of care scope |
| jsp-815 | ch02-sms-structure-and-assurance-stages.md | PDCA basis, Defence Safety Function role, Element / Expectation / Performance Statement hierarchy, ISO 45001 alignment claim, and assurance stages |
| jsp-815 | ch03-leadership-and-organisation.md | Leadership, governance, and culture; organisation and dependencies; SEMS applicability (E1, E2, Annex A) |
| jsp-815 | ch04-legislation-and-exemptions.md | Legislation, policy, regulation and guidance; regulator relationships; exemption certificate process (E3, Annex B) |
| jsp-815 | glossary.md (support file) | Shared Defence safety terms used across the pack, with chapter cross-references |
| jsp-815 | cheatsheet.md (support file) | Cross-chapter decision checklists, all 72 Expectations, exemption steps, safety-case triggers, and audit cycle |

## 2. Risk & Operational Control

| Pack | Chapter | Why it fits / one-line value |
|---|---|---|
| jsp-815 | ch05-risk-assessment-and-safety-cases.md | Risk profile, risk management and elevation, risk communication, change tracking, and safety cases (E4.1 to E4.7) |
| jsp-815 | ch06-supervision-contracting-control.md | Supervision, contracting, control of activity, duty holding, duty of care on deployments, and Head of Establishment (E5, Annexes C and D) |
| jsp-815 | ch07-competence-and-delegation.md | Personnel competence, resources, training, and safety aspects of letters of delegation (E6, Annex E) |
| jsp-815 | ch08-equipment-and-infrastructure.md | Equipment design, manufacture, and maintenance; infrastructure design, build, and maintenance (E7, E8) |

## 3. Performance & Assurance

| Pack | Chapter | Why it fits / one-line value |
|---|---|---|
| jsp-815 | ch09-performance-incidents-communication.md | Performance and management information; accident and incident management and emergency response; communications and stakeholder engagement (E9 to E11) |
| jsp-815 | ch10-assurance-and-audit.md | Assurance and audit, ISO 45001 clause mapping (numbers only), and Annex H audit cycle (E12, Annexes F and H) |
