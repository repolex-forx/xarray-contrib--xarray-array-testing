# Repolex Knowledge Graph of xarray-contrib/xarray-array-testing

RDF knowledge graph data for [xarray-contrib/xarray-array-testing](https://github.com/xarray-contrib/xarray-array-testing), parsed by [repolex](https://repolex.ai).

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
rlex download xarray-contrib/xarray-array-testing
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 8e076665d3d1e7d0a8eb31360d483cd8356ba1c6
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 8e076665d3d1e7d0a8eb31360d483cd8356ba1c6
│           └── chunk-001.nq.gz
├── blob
│   ├── 0ad4b3013cf4acd5ebcee071bfd277c628ec0ef6.nq.gz
│   ├── 0d56b89e8b80a8e23fe3b922260dbd36e0cb8868.nq.gz
│   ├── 51bdd94fff94672a7b543e578c8e575b891f4e11.nq.gz
│   ├── 5f44658d8b47aa521c5bfa821b553710ed6c8cc7.nq.gz
│   ├── 65693d7f6fc391f14e9077884de2a06b379d207c.nq.gz
│   ├── 6833c58e209deb36a2659b28707c29ad0e8272e3.nq.gz
│   ├── 6b3529b87cf92a67fd4e115cd678cfcce5603aee.nq.gz
│   ├── 744ead23b4af3b7553efca5e41a8d35243d44523.nq.gz
│   ├── 8737ab9cbc3a168300cb92c6f73b3d4cede9d012.nq.gz
│   ├── 8a2d4fb61dfacc4cdd9268ba20a81fd2625b990a.nq.gz
│   ├── 9bafaeaf4d3147e0c7530b368571d0ad1b4b58c4.nq.gz
│   ├── 9d1e0987bfc323000b570d680343f00c53ddbc3d.nq.gz
│   ├── a095dc0d8d7b48e01c05f702bfca84574cb2051e.nq.gz
│   ├── ca2db4e6acf8c17a01f4052016b7fd062cc96d20.nq.gz
│   ├── d2f0f1df74d6ef73ee72e9a8329037cf95749a21.nq.gz
│   ├── ea41a1408a441239e1e537468c056a1e7706b478.nq.gz
│   └── fc69ba049f2c9aad2757a8142ba82e2050fff228.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 8e076665d3d1e7d0a8eb31360d483cd8356ba1c6.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 25 files
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

[xarray-contrib/xarray-array-testing](https://github.com/xarray-contrib/xarray-array-testing)

---
*Parsed on 2026-10-28 by [repolex](https://repolex.ai)*
