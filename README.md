# Repolex Knowledge Graph of VoidStarKat/widestring-rs

RDF knowledge graph data for [VoidStarKat/widestring-rs](https://github.com/VoidStarKat/widestring-rs), parsed by [repolex](https://repolex.ai).

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
rlex download VoidStarKat/widestring-rs
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 66dcd7c05ed7de790a1ab0d340b7f4b8b550aed7
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 66dcd7c05ed7de790a1ab0d340b7f4b8b550aed7.nq.gz
│   └── repolex
│       └── 66dcd7c05ed7de790a1ab0d340b7f4b8b550aed7
│           └── chunk-001.nq.gz
├── blob
│   ├── 124e45497ee769dcc5eab555d2e6012878c39d00.nq.gz
│   ├── 251b6bb587c8fa500ffdd0c2b61d66b9841815fc.nq.gz
│   ├── 2886ae4d012da0f89db83717383d63ce4b7387b6.nq.gz
│   ├── 2a8b767d1fddeb9675065d0ca45b2594f71b650d.nq.gz
│   ├── 2a9c2869c995db1cc3d0d5ca3b62ec02627b0af2.nq.gz
│   ├── 371a92d5c5e57b1811b1f36bb9932cea5cbd48e0.nq.gz
│   ├── 39db3e9457c952ef74b09460c4ad5bc40527047a.nq.gz
│   ├── 4320185a404d8f62d5fe58e58ad4e5109fb4d66f.nq.gz
│   ├── 44665de26bd0f20c0abaadedb311810ec00de825.nq.gz
│   ├── 4aa6fc6918a46eef901c7a5525bfd17eb9b4fd3b.nq.gz
│   ├── 4b1e45285f73881fdd966e5fd165a3852e1951db.nq.gz
│   ├── 4b390d80fc3f9e2b530dbff4caff8e3473eb0e62.nq.gz
│   ├── 4cc625773a10d8847cc08c651c9c042f6017fc5f.nq.gz
│   ├── 561931b216d2363f15d23a4ffcba6854146ad4e3.nq.gz
│   ├── 568031ea952d865908e22509c2df10f3e9589ff7.nq.gz
│   ├── 5fb26ca9a19b158f9cfd80e20c9640a74373e62f.nq.gz
│   ├── 6f9227fe9ac2d2ed3413481bb51d258d03c24edb.nq.gz
│   ├── 778692bcb14e40e19107e16464ccd6cd28a2d622.nq.gz
│   ├── 7d945cb05bd1114db3475947ea8af27bacf3f5ad.nq.gz
│   ├── 7db96ca30bb30f6a7bd658ca39cc9ff00c664549.nq.gz
│   ├── 864e52b1c65d7ffd47528514d5ad578a2d17115a.nq.gz
│   ├── 9cf106272ac3b56b0c4c80218e8fc10a664ca5f4.nq.gz
│   ├── 9d2bc1865001a022789ae9af8c6a577c1a3df025.nq.gz
│   ├── ae4f6abc94d0c1039c386451a270a2346615cfb0.nq.gz
│   ├── b61cbb3d93346bc72c378c1c2dd3e94044720b73.nq.gz
│   ├── b7f9e4cf03129daa4ac16874476ae5772ac3a343.nq.gz
│   ├── bf5e37f1bd5b1578f5ed770fa41d4761d0b7aa3b.nq.gz
│   ├── c59c505bbfbfe6f9da8b2b9539c5756cfa3e07b9.nq.gz
│   ├── d9a10c0d8e868ebf8da0b3dc95bb0be634c34bfe.nq.gz
│   ├── e709cfbd82fe0cb0dfc6559eaa8e1931cf29ffc0.nq.gz
│   ├── e81ad6d8ba4fc2975f582c05ecd8578c65f01d07.nq.gz
│   ├── ec468abcdd359bc46d5c599eae91c383c740db95.nq.gz
│   ├── ee2f32889325196f0c4992a44b5511638f36256d.nq.gz
│   ├── f2e401522ce672c2ad8c52063d465ad3224ca833.nq.gz
│   ├── f3c704a075347b9846c539b9a30a57c824221815.nq.gz
│   ├── f4f80064289d366c7d0efad74968e2b8a703acee.nq.gz
│   └── f667b03d4da59a08782509b3a791f289cb736287.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 66dcd7c05ed7de790a1ab0d340b7f4b8b550aed7.nq.gz
├── filetree
│   └── 66dcd7c05ed7de790a1ab0d340b7f4b8b550aed7.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 47 files
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

[VoidStarKat/widestring-rs](https://github.com/VoidStarKat/widestring-rs)

---
*Parsed on 2026-11-23 by [repolex](https://repolex.ai)*
