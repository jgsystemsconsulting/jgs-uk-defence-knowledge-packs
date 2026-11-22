---
name: pack-foldin-hygiene
description: Inventory-hygiene checklist for knowledge-pack fold-ins and landings - every place a chapter-count or inventory change must be reflected beyond PACK.yaml and the five pin sites. Use whenever a fold-in, transplant, or pack landing changes a pack's chapter count, support files, or the repo's pack/signpost inventory.
---

# Pack fold-in hygiene

A chapter-count bump or inventory change touches more than PACK.yaml and the
five gate-pin sites. This checklist exists because the v0.2.0 fold-in missed
four of them and the whole-branch review had to catch each one.

## Trigger

Run this checklist whenever a change does any of:

- folds a new source into an existing pack (chapter count changes)
- lands a new pack or signpost directory
- removes a pack directory
- changes a pack's support-file set (glossary / patterns / cheatsheet)

## The checklist (one commit)

Beyond `PACK.yaml` counters, `catalog.json`, `classification-rules.json`,
`capability-pack-map-note-overrides.json`, and the five pin sites:

1. **`packs/<slug>/LICENSE` chapter range** - the summary line naming the
   chapters built from the source (e.g. "ch01 to ch11") must match the new
   count. Verify any attachment-count sentence still true.
2. **`NOTICE` `[pack: <slug>]` Source line** - must name every source part
   now packaged (folded annexes included), same formatting as the block's
   other fields.
3. **`SKILLS.md` row for the pack** - cover set, chapter claim, and any
   "no Annex X" wording must match the live pack.
4. **`packs/<slug>/SKILL.md` frontmatter description** - the opening cover
   clause (annexes/volumes) must match Scope and Limits. These two strings
   contradicting each other is the defect class that started this checklist.
5. **`docs/index.html`** - the three REV/version loci (masthead, install
   prompt, drafting sheet) on a release cut; Content/Signposts chips on an
   inventory change.
6. **`docs/assets/still-catalogue.svg`** - subtitle, footer, AND the mid
   Content/Signposts count cells (the mid cells are easy to miss; gates pin
   subtitle/footer and mid cells via check_release).
7. **`docs/packs.html`** - rerun `python tooling/gen_packs_page.py`; it
   consumes SKILLS.md, so fix SKILLS.md rows BEFORE regenerating.
8. **`CITATION.cff` + README version loci** - on a release cut, every place
   the old version string appears that the checker does not compare
   (checker coverage: RELEASE-INFO, catalog.json, plugin.json, both website
   YAMLs, index REV loci; CITATION.cff and README are manual).

## Gates after the commit

```
python tooling/validate_pack.py --all
python tooling/check_release.py
python tooling/test_ci_gate.py
```

Fleet repos only: `python tooling/check_pack_slug_dupes.py` (advisory).

## Provenance

Born from jgs-uk-defence-knowledge-packs v0.2.0 final review (6 Important
findings, 4 caused by missed items 1-4 above) and the v0.3.0 fold-in.
