---
name: ukdef
kind: orchestrator
disable-model-invocation: true
description: "Orchestrator (not a knowledge pack): routes a free-text UK Defence question to the right catalogue pack(s), reads them with you, and answers with pack and chapter citations. Runs only on explicit `/ukdef <question>`; carries no source content. Use when you do not know which `/pack` to ask."
---

<!-- argument-hint: [free-text UK Defence question] -->

# UK Defence Orchestrator: routes questions to the right knowledge packs

**This is an orchestrator, not a knowledge pack.** It carries **no source content**.
On explicit `/ukdef <question>` it matches your question to installed catalogue packs,
reads them, and answers with pack and chapter citations.

## When to use
**Prerequisites:** none: plain Markdown; works on any host that loads Agent Skills. Pair it with the packs it routes to.

`/ukdef` answers UK Defence questions by consulting installed packs. It is an
entry point, not a knowledge base. Use it when you do not already know which `/<slug>`
to open.

## How /ukdef answers

### Modes

| Mode | When | Gate |
|---|---|---|
| Narrow consult | One Topics row matches, at most one agency named, no compare/contrast/survey verb | None. Best single pack. End with "Also relevant" runners-up. |
| Broad consult | Two or more Topics rows, two or more agencies, or a compare/contrast/survey verb | One plan approval naming packs and why, then run to done. Disagreements under "Where the sources differ"; never average or blend. |
| Deliverable | An artifact verb (draft, write, produce, prepare, build, review, verify) plus a Deliverables row name or keyword | Plan approval, then stage pauses after Draft and after Review (Verify is last). |

### Routing

1. Match Topics keywords case-insensitively, with synonym judgement.
2. Agency filter: when the question names agencies, keep candidates listed on those Agency contexts rows as long as one survives; otherwise keep all candidates and say no pack from that agency covers the topic.
3. Narrow pick: first-listed pack of the matched row after the filter; if that pack's Scope & Limits flags the question thin, take the next on the row. The consult stays narrow (no gate).
4. Broad pick: best-positioned candidate per named agency, then first-listed of each matched row, then second-listed, stopping at four, or earlier once every matched row and agency is represented and at least two packs are chosen.
5. No match: name the three closest Topics rows, suggest a rephrase or a direct `/<slug>`, and make **no UK Defence claims**.

### Reading

A pack lives at `../<slug>/` from this folder (native installs put members side by side). For each selected pack: read its `SKILL.md` index; open at most two chapters from its Topic Index / Chapter Index; open one support file (`glossary.md`, `patterns.md`, or `cheatsheet.md`) only for term, technique, or decision-rule questions. At most four packs total. If no chapter covers the question, record "no chapter in `slug` covers this" and use the index frameworks where they apply.

Each pack brief returns at most 10 claims of at most two sentences, each with a citation, plus a `thin:` line when Scope & Limits flags the question and a `source:` line copied from the pack's `**Source**` line. No claim from outside its pack.

### Citations and Sources

Cite only files read this session, in these forms: `[slug chNN]`, `[slug index]`,
`[slug glossary|patterns|cheatsheet]`, `[slug signpost]`. Drop uncited claims. Agreeing claims merge into one statement carrying every citation. Where the packs are silent, say so; no fallback to model memory. Every answer ends with a **Sources** block listing each pack's slug, its `**Source**` line, and its licence. Content-pack licences come from the Licences table, else the label `Public Domain (US Government work)`. The jsp-815, jsp-375, and jsp-816 Sources lines carry each pack's `**Source**` Open Government Licence attribution statement, and licence `Open Government Licence v3.0` comes from the Licences table. Signpost lines read `MIT (signpost)`. Identification questions about ISO 45001 ("what is ISO 45001", "where is the text") route to `iso-45001-signpost` only; the answer must **never quote** the standard. Non-commercial and share-alike terms appear in full.

### Deliverable stage chains

The matched Deliverables row is the chain. Draft / Review / Verify cells list the packs for each stage; an empty cell skips that stage (the plan says so). A review or verify request on a user-supplied artifact starts the chain at that stage.

- **Draft** builds the artifact from the Draft packs' guidance with inline citations, then pauses.
- **Review** lists cited findings against the Review packs' criteria and gives the revised artifact, then pauses.
- **Verify** reports a table of item, criterion, result, and citation, plus open items. It edits nothing and offers fixes as a follow-up.

Output goes in the reply unless the user names a file. A deliverable with no matching Deliverables row gets **no improvised chain**: name the closest Deliverables rows or offer a broad consult instead.

### Edge cases

- Bare `/ukdef` with no argument: print usage and three example questions drawn from the Topics rows.
- Sub-agent failure: rerun that brief in the main thread.
- Thin-pack step-down: if the selected pack's Scope & Limits flags the question thin, take the next pack on the row; the consult stays narrow.

## Routing map

<!-- ROUTING-MAP:BEGIN -->
### Topics
| Topic | Keywords | Packs (best first) |
|---|---|---|
| Defence SMS structure and which JSP applies | JSP 815, SMS, safety management system, Defence Safety Function, Safety Operating Model, SofS Policy Statement, JSP 375, JSP 376, JSP 816, JSP 814, duty of care, PDCA, must and should, Expectation, Element, Performance Statement | `jsp-815`, `jsp-375`, `jsp-816` |
| Leadership, governance, safety culture | leadership, governance, Defence Safety Committee, safety culture, tone from the top, Just Culture, Parker-Hudson Ladder, speaking up, corporate governance, accountability | `jsp-815` |
| Organisation and dependencies, SEMS | SEMS, safety management arrangements, Defence Area, FULLCOM, OPCOM, lodge, CSOC, MOU, organisational change, OSA, dependencies and interfaces, contractor standards, consultation, resources | `jsp-815` |
| Legislation, regulators, exemption certificates | legislation, HSWA, SFAIRP, DED, Crown enforcement, statutory regulator, DSA regulators, MAA, DNSR, exemption certificate, ECS, waiver, concession, Combat Immunity | `jsp-815` |
| Risk assessment and safety cases | risk assessment, risk profile, ALARP, tolerability, elevation, golden thread, Risk to Life, RtL, safety case, bow-tie, 5x5 matrix, change management, Principal Safety Risk | `jsp-815` |
| Supervision, contracting, control of activity, duty of care on deployments | supervision, contracting, control of activity, Duty Holding, Duty Holder, EDH, SDH, ODH, DDH, letter of delegation, stop-work authority, safe system of work, SSW, 4Cs, HoE, Head of Establishment, deployment, EIH, FHP, operating risk, operational risk | `jsp-815` |
| Competence, training, letters of delegation | competence, SQEP, training, competency assessment, letter of delegation, Annex E, safety-critical posts, workforce planning, resources, Accountable Person | `jsp-815` |
| Equipment and infrastructure safety | equipment safety, infrastructure safety, CADMID, lifecycle, equipment safety case, platform integration, supply chain, maintenance, operating limits, SRO, design out, modification | `jsp-815` |
| Performance, MI, incident and emergency management | performance, leading indicators, lagging indicators, cultural indicators, management information, MI, trend analysis, accident, incident, near miss, investigation, emergency response, business continuity, stakeholder engagement, anonymous reporting | `jsp-815` |
| Assurance, audit, ISO 45001 mapping | assurance, audit, Annex H, audit manual, 1LOD, 2LOD, 3LOD, Lines of Defence, GIAA, self-assessment, annual assurance report, ISO 45001, clause mapping, enforcement action, ISO 19011 | `jsp-815` |
| Defence H&S arrangements handbook (JSP 375) | JSP 375, health and safety handbook, workplace inspection, first aid, COSHH, DSEAR, permit to work, lone working, heat illness, cold injury, 4Cs contractors, Volume 3 high-risk estate, alternative AMC, safe system of work, MOD Form 5010 | `jsp-375`, `jsp-815` |
| Defence EMS and environmental protection management (JSP 816) | JSP 816, EMS, environmental management system, environmental aspect, BPEO, ISO 14001 alignment, environmental incident, Dir CCE, Element 12 Annex A toolkit, environmental self-assessment | `jsp-816`, `jsp-815` |
| ISO 45001 identification and catalogue location | ISO 45001, what ISO 45001, where ISO 45001 text, OH&S management systems standard catalogue | `iso-45001-signpost` |

### Agency contexts
| Agency | Keywords | Packs |
|---|---|---|
| MOD | MOD, Defence, DDSS, Defence Area, Head of Establishment, UK, Dir DS, Dir CCE | `jsp-815`, `jsp-375`, `jsp-816` |

### Deliverables
| Deliverable | Keywords | Draft | Review | Verify |
|---|---|---|---|---|
| Safety case outline against Element 4 | safety case outline, E4.7, structured argument, system safety, operating environment, ALARP and tolerable | `jsp-815` | `jsp-815` | `jsp-815` |
| Element self-assessment against Expectations | Element self-assessment, Expectation, E12.3, Performance Statement, evidence, assurance level | `jsp-815` | `jsp-815` | `jsp-815` |
| Exemption certificate request checklist | exemption certificate, ECS, Annex B, E3.5, waiver, concession, last resort, residual risk | `jsp-815` | `jsp-815` | `jsp-815` |
| Audit plan per Annex H | audit plan, Annex H, ATL, audit programme, ISO 19011, findings, rating, follow-up | `jsp-815` | `jsp-815` | `jsp-815` |

### Licences
| Pack | Licence |
|---|---|
| `jsp-815` | Open Government Licence v3.0 |
| `jsp-375` | Open Government Licence v3.0 |
| `jsp-816` | Open Government Licence v3.0 |
<!-- ROUTING-MAP:END -->

## Host modes

Pick the highest mode the host can run:

| Mode | When | Behaviour |
|---|---|---|
| Fan-out | Sub-agents available | One brief per pack in parallel; main thread composes the answer. On sub-agent failure, rerun that brief in the main thread. |
| Sequential | No sub-agents, member files readable | Same briefs one at a time; write each pack's notes before opening the next. |
| Index-only | Transform installs (Codex, Gemini, Cursor rules) | Read sibling index files when readable. Cite `[slug index]` only, name chapters as follow-ups, and label the answer `index-level: chapter bodies not installed`. |
| Route-only | No member file readable | Report the routing decision and the `/slug` commands only. Make **no UK Defence claims**. |

**Native-root fallback.** When the skill folder is not revealed, try
`~/.claude/skills/`, `~/.openclaw/skills/`, `~/.copilot/skills/`, each with and
without the `jgs-uk-defence-knowledge-packs/` namespace. Transform index files live at
`~/.codex/prompts/<slug>.md`, `~/.gemini/commands/jgs-uk-defence-knowledge-packs/<slug>.toml`,
and `./.cursor/rules/<slug>.mdc`.

Narrow consults read in the main thread on every host. A missing routed pack is
noted and skipped; if none remain, fall back to route-only.

## Scope & Limits

- No UK Defence claim without a citation from a pack file read this session.
- The map is curated, not exhaustive. Agency rows are a filter, not an endorsement.
- At most six packs per Topics row. At most four packs read per answer.
- Deliverable stage chains come only from Deliverables rows; empty cells skip that stage.
- `/ukdef` never overwrites an existing file without a yes at a gate.
- DEF-STANs (Def Stan 00-051 recorded exclusion / unreachable cover; Def Stan 00-970 not public), JSP 376, JSP 814 remain outside the catalogue; /ukdef names them by title and makes no claims about their content. Neighbouring content packs `jsp-375` and `jsp-816` are in the catalogue; this orchestrator routes to them and makes no claims about those sources beyond what those packs cite. JSP 815 Annex G Assurance Toolkit is folded into `jsp-815` ch11.
- ISO 45001 text is not included. Neighbouring signpost `iso-45001-signpost` covers identification and catalogue location only; this orchestrator routes those questions there and makes no claims about the source beyond what that signpost cites. jsp-815 carries Annex F clause numbers only and must not quote the standard.
- jsp-815, jsp-375, and jsp-816 are reconstructed reference notes, not MOD guidance, and have no official status. This orchestrator makes no claims about JSP 375 or JSP 816 source text beyond routing into those packs.

---
*Orchestrator content © JG Systems Consulting Ltd. (MIT). Pack names and source titles
are identified for routing only; each pack keeps its own licence.*
