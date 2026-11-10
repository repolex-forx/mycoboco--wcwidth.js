# Repolex Knowledge Graph of mycoboco/wcwidth.js

RDF knowledge graph data for [mycoboco/wcwidth.js](https://github.com/mycoboco/wcwidth.js), parsed by [repolex](https://repolex.ai).

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
rlex download mycoboco/wcwidth.js
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 465c404299a523d88d901eee5895e01fabe94225
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 465c404299a523d88d901eee5895e01fabe94225
│           └── chunk-001.nq.gz
├── blob
│   ├── 05e0f4b612078bfff7781e47bfec8e78bae3a7bd.nq.gz
│   ├── 143fe1d228b6f189b1286392d2918e93f73b8b84.nq.gz
│   ├── 24f19bec43c51d2af88b4da2353ada68f46a8fa7.nq.gz
│   ├── 4c88537c43ef0eacdbbc9bca1e11ab20f992aa41.nq.gz
│   ├── 526734d4bc49217d8521985c18410f3b0b858682.nq.gz
│   ├── 55a123d50b84b587fb1a46eda119b4e5195d7c75.nq.gz
│   ├── 64fd6940600bfc3e923c3c306e93e904ec26a906.nq.gz
│   ├── 68658f9bede7eb3602f9df32b548b187b2c8bc7a.nq.gz
│   ├── 9046ce4e575e3dcbeaa4be2e1e8177db314ca09e.nq.gz
│   ├── c2658d7d1b31848c3b71960543cb0368e56cd4c7.nq.gz
│   └── df2bbfba4193f97fc4f33999f1d3c51053881de8.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 465c404299a523d88d901eee5895e01fabe94225.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 19 files
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

[mycoboco/wcwidth.js](https://github.com/mycoboco/wcwidth.js)

---
*Parsed on 2026-11-10 by [repolex](https://repolex.ai)*
