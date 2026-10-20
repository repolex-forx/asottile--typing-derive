# Repolex Knowledge Graph of asottile/typing-derive

RDF knowledge graph data for [asottile/typing-derive](https://github.com/asottile/typing-derive), parsed by [repolex](https://repolex.ai).

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
rlex download asottile/typing-derive
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 67a8d5c2e9df69b237620409dc467f972709ceed
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 67a8d5c2e9df69b237620409dc467f972709ceed
│           └── chunk-001.nq.gz
├── blob
│   ├── 03ec798bda002908dff9b0e41a4afb9160b8d737.nq.gz
│   ├── 2698f6cff906cf7c83101145a12d51bd28f2be24.nq.gz
│   ├── 2b8c82cab73e911914a7020d174b583f7ce0d15d.nq.gz
│   ├── 3570fece9e16d2d3030ef4862e835c39f0f1756c.nq.gz
│   ├── 3d93aefb2da505dba9c0114404cfaaeee5ad0d3f.nq.gz
│   ├── 3e70345b9b408a13b27917590936f046d8674cab.nq.gz
│   ├── 5042c6092df74993a97c82aa5a4ac8341f77985a.nq.gz
│   ├── 569e1008a77368e242be2a4180f4bf29d3b96f42.nq.gz
│   ├── 5fab96db6c0dbf45bfb47fd201ad9601285afbf0.nq.gz
│   ├── 6c4dd943fba994edccfa88757c63ef16bc59f975.nq.gz
│   ├── 77ab823cd07ac65ae2fe53547d4132aba78b5179.nq.gz
│   ├── 77cd687e812c29622f68c5f8ea557320d34a9bf7.nq.gz
│   ├── 90d88bba5662a2a4fa867e7e1c1dbb06b0e0656b.nq.gz
│   ├── 93877692723a7de802a856c30c011d22f805cd5b.nq.gz
│   ├── 9973a41f7650fe7c7a82e9a2795c76de029d0f78.nq.gz
│   ├── a407e0368dc3a56ba52def97082805ab500b461a.nq.gz
│   ├── ab3c4b1e4ad48c2cd8e879f773cd34df0ba94d24.nq.gz
│   ├── ae827f22864143d4e6a40681a04a0fffc676cb44.nq.gz
│   ├── bd8fd67bd3785cf04fccc927a947ffd37e3272aa.nq.gz
│   ├── c9ff51f56bdf36e5445d4a12867cff6fb83c68ed.nq.gz
│   ├── ca1d90ea180858ae143c0e62d920e350d3acc62d.nq.gz
│   ├── e56ef64e09fa1d131e1440b05ac9b9256929d6ba.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── eae037512c53a13a3e8902090ab78dfe968dfe36.nq.gz
│   ├── ed093b48cc8c8fadabb0ff1adaeab8585297d349.nq.gz
│   ├── f7f905f1dac4f1c941fb34e17a38ee65dd89ca57.nq.gz
│   └── f8d3dcb11568b3f5712a3279f558fdf43356b8e1.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 67a8d5c2e9df69b237620409dc467f972709ceed.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 35 files
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

[asottile/typing-derive](https://github.com/asottile/typing-derive)

---
*Parsed on 2026-10-20 by [repolex](https://repolex.ai)*
