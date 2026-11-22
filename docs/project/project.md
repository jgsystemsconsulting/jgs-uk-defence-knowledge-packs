# Project

## goals
status: accepted
source: 2026-11-22-uk-defence-knowledge-pack-elaboration

The UK defence sector catalogue ships licence-clean agent reference packs from vetted UK defence sources, with one orchestrator that routes to them. Each UK defence publication has one canonical content pack in this repo. Sibling sectors keep their own sources and do not carry a second content copy of a publication this repo owns.

## scope
status: accepted
source: 2026-11-22-uk-defence-knowledge-pack-elaboration

In this repo: pack trees under packs/, the ukdef orchestrator, catalog.json, sector docs, the release train, and the gates. Out: the systems-engineering catalogue, the nuclear catalogue, hub installer copies of these packs, and redistributed source originals. sources/ does not hold those originals. A sibling sector is not folded into this repo.

## glossary
status: accepted
source: 2026-11-22-uk-defence-knowledge-pack-elaboration

Content pack: a packs/<slug>/ tree with chapters, reconstructed from one vetted source.
Signpost: a pack with kind signpost, citation only, and no reproduced source text.
Orchestrator: the single router, slug ukdef, with no source content.
Absorption: folding one sector catalogue into another. Forbidden. A pack that belongs in another sector is authored or moved under that sector's release train.
Fold-in: the reference-skill update that merges a newly vetted source into an existing pack, bumps build counters, and re-verifies the gates.
