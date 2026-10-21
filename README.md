# Repolex Knowledge Graph of scikit-image/skimage-branding

RDF knowledge graph data for [scikit-image/skimage-branding](https://github.com/scikit-image/skimage-branding), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [rlex](https://github.com/repolex-ai/rlex) query tool:

```bash
cargo install --git https://github.com/repolex-ai/rlex
```

Verify the install:

```bash
rlex --help
```

**rlex is designed to be used primarily by LLMs in a terminal.** Start up your favorite AI assistant and ask it to use rlex. It handles the SPARQL — you just ask questions in plain English.

To load this repo's data:

```bash
rlex download scikit-image/skimage-branding
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 4265eec74b1ecd6273c27b1ca6cfecf5e1f3a3ef
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 4265eec74b1ecd6273c27b1ca6cfecf5e1f3a3ef
│           └── chunk-001.nq.gz
├── blob
│   ├── 050ce1a692eb2369864496b4b90a666690f99c5c.nq.gz
│   ├── 06f4baba4ed214d99ab029dd3a1d172e303db43d.nq.gz
│   ├── 1cf861bdf10b1ac3072d09b6569d4da15b5cef52.nq.gz
│   ├── 205e1bf4d23802df62ad410ae387755a935d4587.nq.gz
│   ├── 3ae5d0c1ba6afdacd3d7991fdfcc52d2aa9bb65b.nq.gz
│   ├── 5f9f634f7fd94a58fd9bc55f788710a670733569.nq.gz
│   ├── 6f72eb809c491d7bfb62867dd55a3ac1094c13ba.nq.gz
│   ├── 72fa05086118ec2bcea9985e93dc1cdc8990919a.nq.gz
│   ├── 8025bc04008ce3548567fde9e986380c54bc33c8.nq.gz
│   ├── 8cd6a3ae4c72318158b387fe03c54d373bf5521d.nq.gz
│   ├── 977b3266f467a649ede1cab71fb2c971c8920e07.nq.gz
│   ├── b23787c8fdf09ae6b6555052e3e8ce17b1622595.nq.gz
│   └── cb3c337c016fbaaf5609c96ad5b53ddd803e3d73.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 4265eec74b1ecd6273c27b1ca6cfecf5e1f3a3ef.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 21 files
```

| Directory | What it contains |
|-----------|-----------------|
| `blob/` | Per-file AST graphs, content-addressed by git blob SHA. Each file in the source repo gets its own graph. |
| `aggregate/ast/` | Combined AST graph per parsed commit. Merges all blob graphs for a snapshot of the entire codebase at that point. |
| `aggregate/lsp/` | Language Server Protocol enrichment: resolved symbols, definitions, references, and type information. |
| `aggregate/dataflow/` | Interprocedural data flow edges between functions and modules. |
| `aggregate/repolex/` | Combined graph (AST + LSP + dataflow) per commit. |
| `commit/` | Git commit metadata (author, date, message, parent links). |
| `branch/` | Branch metadata. |
| `tag/` | Tag metadata. |
| `filetree/` | File tree snapshots per commit (which files existed and their blob SHAs). |
| `audit/` | Code architecture and graph audit reports per commit. |

## Source repository

[scikit-image/skimage-branding](https://github.com/scikit-image/skimage-branding)

---
*Parsed on 2026-10-21 by [repolex](https://repolex.ai)*
