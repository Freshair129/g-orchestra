# Split notes

This repository was split out of `Freshair129/G-Maiden` (`orchestration/`) on 2026-11-06
with its history (`git subtree split`, 57 commits, 262 files). Tracking issue:
Freshair129/G-Maiden#134.

## Known gaps after the split

- `POST /api/search` needs `tools/doc-graph/semantic_ir.mjs`, which stays in G-Maiden. Set
  `GMAIDEN_ROOT` to a G-Maiden checkout to enable it; otherwise the route returns 501.
  Other routes are unaffected.
- `server.mjs` also reads `docs/DOC-GRAPH.json` (see `DOC_GRAPH_FILE`), produced by
  `tools/doc-graph/scan.mjs` in G-Maiden.
- Documents here may still link to G-Maiden paths (`docs/…`, `src-tauri/…`) that
  are no longer relative to this repository. They were not rewritten.
- `.github/` workflows from G-Maiden were not copied.
