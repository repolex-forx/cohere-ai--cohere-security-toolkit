# Repolex Knowledge Graph of cohere-ai/cohere-security-toolkit

RDF knowledge graph data for [cohere-ai/cohere-security-toolkit](https://github.com/cohere-ai/cohere-security-toolkit), parsed by [repolex](https://repolex.ai).

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
rlex download cohere-ai/cohere-security-toolkit
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── fb385ad2b70c6379782088261d23eb97e6950317
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── fb385ad2b70c6379782088261d23eb97e6950317
│           └── chunk-001.nq.gz
├── blob
│   ├── 25b23b21fbf61c33176c3b9a19aa61133fc2371b.nq.gz
│   ├── 28d3c48d4eca931d7894a4131cb0fc4c012e59dd.nq.gz
│   ├── 3cd54859daf7e2c13b64b234f3c38dbd64d008d8.nq.gz
│   ├── 6ad8401ecd203edd4f252b576a5e65d8c935246d.nq.gz
│   ├── 7c0545d504c29208630662826dc8d6e0e733ecb9.nq.gz
│   ├── 7e2640417cb48c9818a8d858e50a419a090fa53c.nq.gz
│   ├── 917dd92902d2694b05b8e3c76b5ab915b0333650.nq.gz
│   ├── 981eac31410aa62b2b7188cb3a40ca8e23ea8ae3.nq.gz
│   ├── b4d6da604430d7a43163e5be86bf1e6a985e9f1f.nq.gz
│   ├── c0b2f194342d6eaa059f85cc3c79c3b8e08c681a.nq.gz
│   ├── ddb4dd21a28bb7fa616d087f22d2d190091ecdde.nq.gz
│   ├── fab2036c178fa68711757c26d4e30c549e2e80ec.nq.gz
│   └── fffb5918edbf20be2a0324057e299b61ce36a711.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── fb385ad2b70c6379782088261d23eb97e6950317.nq.gz
├── issue
│   └── issue.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 20 files
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

[cohere-ai/cohere-security-toolkit](https://github.com/cohere-ai/cohere-security-toolkit)

---
*Parsed on 2026-11-08 by [repolex](https://repolex.ai)*
