# Repolex Knowledge Graph of holoviz/jupyter-panel-proxy

RDF knowledge graph data for [holoviz/jupyter-panel-proxy](https://github.com/holoviz/jupyter-panel-proxy), parsed by [repolex](https://repolex.ai).

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
rlex download holoviz/jupyter-panel-proxy
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── d1a929931268ea96ad4074fe5fe2c1d11d4fb4af
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── d1a929931268ea96ad4074fe5fe2c1d11d4fb4af
│           └── chunk-001.nq.gz
├── blob
│   ├── 14571c0bdb1aeb6368254871a37436f4d7f08bef.nq.gz
│   ├── 3e39800f54b0540b766a3c622da045c553962d0e.nq.gz
│   ├── 453936096ba0c6b388b57485943065a82f69f836.nq.gz
│   ├── 6a1a36734f20ccd3c580d4163217a7704523b32f.nq.gz
│   ├── a30ddd9cc77186db1ff00f456911ad4c2cc65ddf.nq.gz
│   ├── a365c0d76f3e5a846125760c17f10ed6a3121cda.nq.gz
│   ├── a64af2f422e89b9f197b4400ce7dc7db83e06e99.nq.gz
│   ├── ae4ffbfb0e65e3591b6431edd00cd16f25a06d4b.nq.gz
│   ├── b347c393bebd72d3959a63e854e9bfb7a977e878.nq.gz
│   ├── dddb91b8e9692c3203f8b33c3b01dba2c6f84bd7.nq.gz
│   ├── dec1f43251435af8fef5f81c1e1fc0ced5782c42.nq.gz
│   ├── e53d969180160a0b6c7dea392250da05fc4bb629.nq.gz
│   ├── e6a7440baee0f7c0d1f8393f3b031451a927b8c1.nq.gz
│   ├── f82f53700a941ffebd4cd43c9a38590206746aa9.nq.gz
│   └── fe004dee397c2dd75e0c27ab8a261783bd58b3f0.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── d1a929931268ea96ad4074fe5fe2c1d11d4fb4af.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 23 files
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

[holoviz/jupyter-panel-proxy](https://github.com/holoviz/jupyter-panel-proxy)

---
*Parsed on 2026-10-21 by [repolex](https://repolex.ai)*
