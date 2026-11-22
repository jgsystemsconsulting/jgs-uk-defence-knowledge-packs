# Requirements

## req-1
status: verified
source: 2026-11-22-uk-defence-knowledge-pack-elaboration

After the owning-sector move, each UK defence publication packaged as content has one canonical pack in this repo. A sibling repo does not keep a content pack with the same slug.

## req-2
status: verified
source: 2026-11-22-uk-defence-knowledge-pack-elaboration

A source on the Excluded tier is not packaged as chapters. The sanctioned published form is a signpost. If no signpost is warranted, the source stays out of packs/.

## req-3
status: verified
source: 2026-11-22-uk-defence-knowledge-pack-elaboration

This repo has exactly one orchestrator: packs/ukdef, kind orchestrator. Its routing map covers every content pack in the repo.

## req-4
status: verified
source: 2026-11-22-uk-defence-knowledge-pack-elaboration

A release tag is cut only when tooling/validate_pack.py on every pack, tooling/check_release.py, and tooling/test_ci_gate.py exit 0, and those checks match .github/workflows/validate.yml. Content generation also passes the reference-skill step 9 gates from jgs-reference-skill: n-gram overlap, pack_eval, and scan_generated_skill. Those programs are not this repo's tooling/check_overlap.py, which checks chapter-basename collisions.
