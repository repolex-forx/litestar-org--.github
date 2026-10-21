# Repolex Knowledge Graph of litestar-org/.github

RDF knowledge graph data for [litestar-org/.github](https://github.com/litestar-org/.github), parsed by [repolex](https://repolex.ai).

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
rlex download litestar-org/.github
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 0c0a5f01bbd7e34fa4bc02bd314207004fb78a78
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 0c0a5f01bbd7e34fa4bc02bd314207004fb78a78
│           └── chunk-001.nq.gz
├── blob
│   ├── 00fba7f93d45af3d8d8c3740a6dad37f28f2bdd7.nq.gz
│   ├── 02b4dd0c499a3222d225dfda03ac6177d984b8c6.nq.gz
│   ├── 0660aa8bcafb9b492e4186c7311a5eaf29024fbb.nq.gz
│   ├── 1185c797bf3f3e781822c6d73556b0541192e775.nq.gz
│   ├── 1abd6eb4c006dd145861a213015de2f223619824.nq.gz
│   ├── 292b09368bebcd904590b42a7be8c7bfc1d7f9e8.nq.gz
│   ├── 41e3cce5b192b37e7f5a4c4027316c3685f6544f.nq.gz
│   ├── 5038c1d017a5a5a7cd5fcd321f054bd2a40a5cc3.nq.gz
│   ├── 6c97be0d364b4055420de63de1cd24ef4d98a74b.nq.gz
│   ├── 72ac56b568dd0384ea3b6bcd935d1c276d57d82e.nq.gz
│   ├── 90446afc3da119a8cdeadaee892c7a70768b84d9.nq.gz
│   ├── 97205b394f4f5ec0587dfa85d85917355f6316cf.nq.gz
│   ├── b642b146d6556cf6a4ccf65d8c90298a00e3564a.nq.gz
│   ├── bdf80297995c717d44ece96a43421a0708f6a023.nq.gz
│   ├── c5ba3b7ec0be0ed3f0ee09b5364ece3b20321bd3.nq.gz
│   ├── cf06aeed9d86884c093e22309fe17c9f38c0e6e2.nq.gz
│   ├── fbc9b21c74f9f6ad7563d6f432dae1c7a58e2f57.nq.gz
│   └── fe016e6d833b1d2f8ba27907bbcbcf1aed9c22c3.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 0c0a5f01bbd7e34fa4bc02bd314207004fb78a78.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 26 files
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

[litestar-org/.github](https://github.com/litestar-org/.github)

---
*Parsed on 2026-10-21 by [repolex](https://repolex.ai)*
