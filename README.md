# Repolex Knowledge Graph of aio-libs/aiosparql

RDF knowledge graph data for [aio-libs/aiosparql](https://github.com/aio-libs/aiosparql), parsed by [repolex](https://repolex.ai).

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
rlex download aio-libs/aiosparql
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── f90ed49df5c7ca624fcb420292ab4e5ffc860227
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── f90ed49df5c7ca624fcb420292ab4e5ffc860227
│           └── chunk-001.nq.gz
├── blob
│   ├── 06402c368247a731ce2e7d919feab7d8d63f283c.nq.gz
│   ├── 086105e6abf1efce442dd0d9d4247e4e00c6ae0b.nq.gz
│   ├── 0cb821f6e787ca787caa042f2482b2c266623d97.nq.gz
│   ├── 157f450e0c4517645ea1ee9084daa87c9b8d2a13.nq.gz
│   ├── 26f559925f3f7d04e9cf7ce4e405f8f28322ae62.nq.gz
│   ├── 3722e70e7db993c8e5441b56d009ba21c200a811.nq.gz
│   ├── 5c072db2b3fe4851faaad503183f911d1af26c9c.nq.gz
│   ├── 7a37a73411d9da27cf86e92ae2e085a38421dbb3.nq.gz
│   ├── 8f2bdd959da9765877b5ed8053a712ad28008d32.nq.gz
│   ├── 96dd3a2795e700bb3b62889c2f511be263ca5114.nq.gz
│   ├── 9704e51097f5ed95e7eeda6e73eb84f611b20874.nq.gz
│   ├── 9975426da6ca4f711932ee751aeabbd5fdc7150a.nq.gz
│   ├── 9ac760cd3b2a30a19d0904fda773b6c93e0b35ca.nq.gz
│   ├── a3dd1fef8512f14223606634dc2213763be0f589.nq.gz
│   ├── aa0d2275f2e2cfcce787c39b13f3cdc5fb1c88c8.nq.gz
│   ├── cc01c719a476e1df08aad5dd485448cfd25041dd.nq.gz
│   ├── d2b6f85593c12318004df01b0dbe10356c4ed359.nq.gz
│   ├── d723b8dd5b48b687d0f2bc98bc23e726eda5170f.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e7b16d17878c4ee65a75aceb1bd3ec4d9131c58d.nq.gz
│   ├── ea370a8e55e9af5fcda45d1f12372a47d86f1a69.nq.gz
│   ├── f31b7d9ea197482ef08fffcbdf4b39dcfebddc29.nq.gz
│   └── f54ad9e77c12235ed2b6851cf7a8d8c0158d51bf.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── f90ed49df5c7ca624fcb420292ab4e5ffc860227.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 31 files
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

[aio-libs/aiosparql](https://github.com/aio-libs/aiosparql)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
