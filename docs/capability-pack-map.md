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
| 1. Safety Management Framework & Governance | 15 |
| 2. Risk & Operational Control | 17 |
| 3. Performance & Assurance | 9 |
| **Total** | **41** |

## 1. Safety Management Framework & Governance

| Pack | Chapter | Why it fits / one-line value |
|---|---|---|
| jsp-815 | ch01-defence-safety-jsp-map.md | Which JSP answers what: JSP 815 SMS, JSP 816 EMS, JSP 375, JSP 376, JSP 814, SofS Policy Statement, Safety Function Operating Model, DSA regulators, and duty of care scope |
| jsp-815 | ch02-sms-structure-and-assurance-stages.md | PDCA basis, Defence Safety Function role, Element / Expectation / Performance Statement hierarchy, ISO 45001 alignment claim, and assurance stages |
| jsp-815 | ch03-leadership-and-organisation.md | Leadership, governance, and culture; organisation and dependencies; SEMS applicability (E1, E2, Annex A) |
| jsp-815 | ch04-legislation-and-exemptions.md | Legislation, policy, regulation and guidance; regulator relationships; exemption certificate process (E3, Annex B) |
| jsp-815 | glossary.md (support file) | Shared Defence safety terms used across the pack, with chapter cross-references |
| jsp-815 | cheatsheet.md (support file) | Cross-chapter decision checklists, all 72 Expectations, exemption steps, safety-case triggers, and audit cycle |
| jsp-815 | patterns.md (support file) | Support file: techniques already stated in the jsp-815 chapters present in this commit |
| jsp-816 | ch01-ems-framework-purpose-and-authority.md | EMS Framework purpose, SofS authority, jurisdiction. |
| jsp-816 | ch02-ems-structure-pdca-and-assurance-stages.md | PDCA, 12 Elements hierarchy, ISO 14001 alignment claim, assurance stages. |
| jsp-816 | ch03-leadership-governance-organisation.md | E1 leadership/culture and E2 organisation/dependencies. |
| jsp-816 | ch04-legislation-policy-exemptions.md | E3 legislation, policy, exemptions/disapplications. |
| jsp-816 | glossary.md (support file) | EMS terms glossary (support). |
| jsp-375 | ch01-directive-structure-and-use.md | JSP 375 handbook structure, ownership, Directive/Guidance. |
| jsp-375 | ch02-scope-assurance-amc-coherence.md | Scope, alternative AMC, assurance via JSP 815, coherence. |
| jsp-375 | glossary.md (support file) | JSP 375 terms glossary (support). |

## 2. Risk & Operational Control

| Pack | Chapter | Why it fits / one-line value |
|---|---|---|
| jsp-815 | ch05-risk-assessment-and-safety-cases.md | Risk profile, risk management and elevation, risk communication, change tracking, and safety cases (E4.1 to E4.7) |
| jsp-815 | ch06-supervision-contracting-control.md | Supervision, contracting, control of activity, duty holding, duty of care on deployments, and Head of Establishment (E5, Annexes C and D) |
| jsp-815 | ch07-competence-and-delegation.md | Personnel competence, resources, training, and safety aspects of letters of delegation (E6, Annex E) |
| jsp-815 | ch08-equipment-and-infrastructure.md | Equipment design, manufacture, and maintenance; infrastructure design, build, and maintenance (E7, E8) |
| jsp-816 | ch05-aspects-risk-impact-opportunities.md | E4 aspects, risk/impact, opportunities, environmental cases. |
| jsp-816 | ch06-ems-supervision-contracting-control.md | E5 supervision, BPEO, stop-work, contracting control. |
| jsp-816 | ch07-competence-resources-training.md | E6 competence, resources, training. |
| jsp-816 | ch08-ems-equipment-and-infrastructure.md | E7-E8 equipment and infrastructure lifecycle EP. |
| jsp-816 | patterns.md (support file) | EMS stand-up and assurance patterns (support). |
| jsp-375 | ch03-risk-assessment-and-safe-systems-of-work.md | Vol 1 Ch 8 risk assessment and safe systems of work. |
| jsp-375 | ch04-workplace-basics-emergency-first-aid-inspections.md | Workplace basics: emergency, inspections, first aid, traffic. |
| jsp-375 | ch05-hazardous-substances-dsear-asbestos-legionella.md | Hazardous substances, DSEAR, asbestos, legionella. |
| jsp-375 | ch06-physical-hazards-equipment-energy.md | Physical/energy hazards, PTW, confined spaces, height. |
| jsp-375 | ch07-people-factors-oh-ppe-vulnerable-groups.md | OH surveillance, PPE/RPE, stress, vulnerable groups, DSE. |
| jsp-375 | ch09-military-training-heat-cold-force-health.md | Military training, heat/cold injury, force health protection. |
| jsp-375 | ch10-volume3-high-risk-estate-activities.md | Volume 3 high-risk estate activities overview. |
| jsp-375 | patterns.md (support file) | Directive-first and 4Cs patterns (support). |

## 3. Performance & Assurance

| Pack | Chapter | Why it fits / one-line value |
|---|---|---|
| jsp-815 | ch09-performance-incidents-communication.md | Performance and management information; accident and incident management and emergency response; communications and stakeholder engagement (E9 to E11) |
| jsp-815 | ch10-assurance-and-audit.md | Assurance and audit, ISO 45001 clause mapping (numbers only), and Annex H audit cycle (E12, Annexes F and H) |
| jsp-815 | ch11-assurance-self-assessment-toolkit.md | Annex G Assurance Self-Assessment Toolkit method, scoring bands, and document-list aides for 1LOD self-assessment |
| jsp-816 | ch09-performance-incidents-communications.md | E9-E11 performance MI, incidents, stakeholders. |
| jsp-816 | ch10-assurance-lines-of-defence.md | E12 three lines of defence assurance. |
| jsp-816 | ch11-ep-self-assessment-toolkit.md | Element 12 Annex A EP self-assessment toolkit method. |
| jsp-816 | cheatsheet.md (support file) | Element routing cheatsheet (support). |
| jsp-375 | ch08-contractors-change-occurrences-records.md | 4Cs contractors, MoC, occurrence reporting, records. |
| jsp-375 | cheatsheet.md (support file) | Topic routing cheatsheet (support). |
