# Repolex Knowledge Graph of pradyunsg/sphinx-inline-tabs

RDF knowledge graph data for [pradyunsg/sphinx-inline-tabs](https://github.com/pradyunsg/sphinx-inline-tabs), parsed by [repolex](https://repolex.ai).

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
rlex download pradyunsg/sphinx-inline-tabs
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 7ee04d209dd1ad4b0f7fa71ece040e9993abba6a
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 7ee04d209dd1ad4b0f7fa71ece040e9993abba6a
│           └── chunk-001.nq.gz
├── blob
│   ├── 01a4f1f4ad83aa63c6630c9834c0ab8622751ee9.nq.gz
│   ├── 02429d54fa4e5aefb361d672b4cd7cb125ed1d61.nq.gz
│   ├── 08bf877460d4179a76eb83286a71974c40d08add.nq.gz
│   ├── 13042e567208006f540374a7d89a606c063a39bf.nq.gz
│   ├── 15099f64fba74880decaa995780747b5ce5ed98e.nq.gz
│   ├── 166920f7d39c53c65f5c9a8f6845642816022332.nq.gz
│   ├── 1c187bdeda11775497b1f018c833681b3ffd63a1.nq.gz
│   ├── 1c2615c484253403add46fcd129229bbb810e226.nq.gz
│   ├── 2b40bb4efb8db2eb257622fc922be6df72ea037d.nq.gz
│   ├── 2dd9455dbdb15b46705b5795017f135b177f1693.nq.gz
│   ├── 4ff67dc53575c045b64d9afb81216fd699acf737.nq.gz
│   ├── 58be2d2f4f81f0a6785d201da75fb7b93682033b.nq.gz
│   ├── 58d2cdddd48beec0fd65c80702d4ae8c3c1a987d.nq.gz
│   ├── 5c28d868c57302f5a583007167a793edc385940d.nq.gz
│   ├── 7afdf76435bb55a80cba0f9da8a557d9623e8089.nq.gz
│   ├── 8d8bc53f2d02961ae7147fdc5c5746f789ebd204.nq.gz
│   ├── 9410c79428da40f9b460343932d8f46cd1ad63c8.nq.gz
│   ├── 968e253806b12460f2a4761c64f95806b9d4b5dc.nq.gz
│   ├── 9e836bb9fc1c5486b1286769f1520d4112ed78aa.nq.gz
│   ├── a39eb4ce8874441b851fc9536fac54d8d9454fbe.nq.gz
│   ├── a7ba02dbe77e080e63316c6db06facaee9ca3dab.nq.gz
│   ├── b2ab9cb76f181a0131e2c39792ee3a6bc4c02e7e.nq.gz
│   ├── b8eeb5e4143bad1b32268ff5955e8599223e44ce.nq.gz
│   ├── b9fb3f3e8caa50cb46d61e0d193bad2624b598c9.nq.gz
│   ├── c71a6ea8d0b58c90cb321a4d3c9bc68c9a1b60e9.nq.gz
│   ├── c7d9aac938c00423a4059100e680050cbd105d9d.nq.gz
│   ├── d4f867d737d2e0f1a27d3ad54cfa0e9672613c78.nq.gz
│   ├── d919754595f482a2f926fa740730b9a4eff5d57a.nq.gz
│   ├── e21089012e095d283a9e5890e56aa0fb8dc9d653.nq.gz
│   ├── f49057c211b6a2e89acb54a8a93ff05684f7e7d3.nq.gz
│   └── f4fabc5d6bffda9d0ebb55eb81d411fdefb864e2.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 7ee04d209dd1ad4b0f7fa71ece040e9993abba6a.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 39 files
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

[pradyunsg/sphinx-inline-tabs](https://github.com/pradyunsg/sphinx-inline-tabs)

---
*Parsed on 2026-11-06 by [repolex](https://repolex.ai)*
