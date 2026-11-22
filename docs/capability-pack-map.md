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
| 1. Safety Management Framework & Governance | 29 |
| 2. Risk & Operational Control | 30 |
| 3. Performance & Assurance | 13 |
| **Total** | **72** |

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
| jsp-376 | ch01-acquisition-safety-policy.md | JSP 376 policy frame: ALARP, tolerability, exemptions, and the six acquisition safety concepts |
| jsp-376 | ch02-roles-and-safety-in-the-programme.md | SRO and User safety accountabilities, the programme envelope, and the unpublished Chapter 4 gap |
| jsp-376 | glossary.md (support file) | Support file: glossary.md for jsp-376 |
| jsp-376 | cheatsheet.md (support file) | Support file: cheatsheet.md for jsp-376 |
| jsp-912 | ch01-what-is-hfi-and-why-defence-mandates-it.md | What Human Factors Integration is and why Defence policy mandates it across acquisition and through-life management |
| jsp-912 | ch02-roles-and-responsibilities.md | HFI roles and responsibilities for programme teams, HFI practitioners, and senior stakeholders |
| jsp-912 | ch09-competencies-ethics-conduct.md | HFI practitioner competencies and standards for research ethics and professional conduct |
| jsp-912 | glossary.md (support file) | Support file: glossary.md for jsp-912 |
| jsp-912 | cheatsheet.md (support file) | Support file: cheatsheet.md for jsp-912 |
| jsp-936 | ch01-introduction.md | Policy, scope, applicability, and tailoring direction for dependable AI from JSP 936 Part 1 |
| jsp-936 | ch02-ai-in-defence-systems.md | How AI including RAS and digital systems is framed inside Defence systems from JSP 936 Part 1 |
| jsp-936 | ch03-legal-ethics-governance.md | Legal, ethics, and governance direction for AI-enabled capability from JSP 936 Part 1 |
| jsp-936 | glossary.md (support file) | Support file: glossary.md for jsp-936 |
| jsp-936 | cheatsheet.md (support file) | Support file: cheatsheet.md for jsp-936 |

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
| jsp-376 | ch03-safety-management-and-requirements.md | Safety Management Plan, safety KUR, and URD and SRD safety requirements across the lifecycle |
| jsp-376 | ch06-early-lifecycle-phases.md | Pre-Concept, Concept, and Assessment safety artefacts and SOC, OBC, and FBC evidence |
| jsp-376 | ch07-demonstration-and-manufacture.md | Demonstration evidence, Manufacture handover, and Duty Holder appointment before in-service |
| jsp-376 | ch08-in-service-and-disposal.md | In-service safety case reviews, the two-year review ceiling, and disposal and termination |
| jsp-912 | ch03-hfi-and-systems-engineering.md | HFI within the systems engineering life cycle and links to DLODs and System Readiness Levels |
| jsp-912 | ch04-hfi-process-goals-activities-tailoring.md | HFI process goals and activities and how to tailor them to project scale and novelty |
| jsp-912 | ch05-user-need-and-system-requirements.md | User needs and HFI system requirements through processes HFI-1.0 and HFI-2.0 |
| jsp-912 | ch06-assess-tenders-hfi-3-0.md | Assessment of contractor tenders for human factors capability through process HFI-3.0 |
| jsp-912 | ch07-detailed-system-design-hfi-4-0.md | Human factors data applied to detailed system design through process HFI-4.0 |
| jsp-936 | ch04-human-ai-teams.md | Human and AI teaming expectations across roles and human control from JSP 936 Part 1 |
| jsp-936 | ch05-ai-lifecycles.md | Lifecycle direction for developing, deploying, and retiring AI systems from JSP 936 Part 1 |
| jsp-936 | ch06-quality-safety-security.md | Quality, safety, and security expectations for AI systems from JSP 936 Part 1 |
| jsp-936 | ch07-suppliers.md | Supplier and procurement direction for acquiring AI systems from JSP 936 Part 1 |

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
| jsp-376 | ch04-test-evaluation-and-safety-case.md | ITEAP, certification strategy, and safety case ownership from Pre-Concept to handover |
| jsp-376 | ch05-supervision-assurance-approvals.md | Three lines of defence, the Safety Assurance Model, and safety inside the five-case business case |
| jsp-912 | ch08-test-acceptance-in-service-feedback.md | Test and acceptance of HFI requirements and in-service feedback through HFI-5.0 and HFI-6.0 |
| jsp-936 | ch08-ai-assurance.md | Assurance expectations and evidence for dependable AI claims from JSP 936 Part 1 |
