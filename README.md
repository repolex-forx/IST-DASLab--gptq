# Repolex Knowledge Graph of IST-DASLab/gptq

RDF knowledge graph data for [IST-DASLab/gptq](https://github.com/IST-DASLab/gptq), parsed by [repolex](https://repolex.ai).

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
rlex download IST-DASLab/gptq
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 2d65066eeb06a5c9ff5184d8cebdf33662c67faf
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 2d65066eeb06a5c9ff5184d8cebdf33662c67faf
│           └── chunk-001.nq.gz
├── blob
│   ├── 0a2a924d67d7f81d6d392a6ac3dd871f6a5a7cb5.nq.gz
│   ├── 0ad6e897a2cf2e5f83d6ad732e432079a80d89a1.nq.gz
│   ├── 0c5d12b16c85aac81394418f41a8f3b4d4ee4de2.nq.gz
│   ├── 0f9af66e12424051380eac8df4ec22e496089d2c.nq.gz
│   ├── 101167f06f333222454e2f030de5ce60d03285af.nq.gz
│   ├── 11f70500fbb49628a8aaf3e1c1b1e18e7373cc34.nq.gz
│   ├── 1816812b2481dd4d3e8252ad2941be874862bcb2.nq.gz
│   ├── 193953c55fb9fa67e617f594a9b0cbfb37f47554.nq.gz
│   ├── 1bf08941fdaa3bea9dc26cbd2fd49fe61c0740c4.nq.gz
│   ├── 1fa90c46abf2968ae1f3a9937dc5bb128714017c.nq.gz
│   ├── 234b752ecf9f5986158868399791bf035fee7556.nq.gz
│   ├── 261eeb9e9f8b2b4b0d119366dda99c6fd7d35c64.nq.gz
│   ├── 286533032bc8cce6947ac49bab05a89eb9fe8d58.nq.gz
│   ├── 2c940a0c5d278e3b760b6783e8b04c60a4c6d0fe.nq.gz
│   ├── 36a11c207d41cf1f2e270c1772488b9a90ae6da0.nq.gz
│   ├── 45b723b603f0ac05aabe549a13cace6b3edf5925.nq.gz
│   ├── 4a1592962aab0c5f2fb4eca78dda8b63b5d5c83f.nq.gz
│   ├── 506bef8279c4cea9836b62021543e40855c81e8e.nq.gz
│   ├── 64387acda8033030dfa7b5df80e4e2cb5824c882.nq.gz
│   ├── 6f05634c8e4f27672410795e1543b4b42ad0d68b.nq.gz
│   ├── 70ad883423cf50a29554bbfebc76d51b299aca71.nq.gz
│   ├── 73d7e1884a1dbfe3f7604f6de4b0c2a9ac030fe1.nq.gz
│   ├── 7b11c980b1b58b7bf9c7ed4420587ec82e7f57a1.nq.gz
│   ├── 855c6aef53176900285ef5a4dae05e2011a5df97.nq.gz
│   ├── 8ee83187f561d9735ebebb06e20d03cac290dd79.nq.gz
│   ├── 8f30a426959d0adb4a2a298e259995758c4cd819.nq.gz
│   ├── 9867d90681d7bbfb130f6842b45a4e3ce508b5df.nq.gz
│   ├── 9b478c58eb30c0f60eaa29437199032639aa42a1.nq.gz
│   ├── a034af18493cec3ff3bc9f4a3b25bcc9104f25ab.nq.gz
│   ├── a6cd26f81b50bac8dcecff4d382b6737f00c4bea.nq.gz
│   ├── addc8d974ef4f4ce4fe7627301f2530c4379d35d.nq.gz
│   ├── ae269756f62806b6640bc0cf7a509e9833c07fb3.nq.gz
│   ├── bb7004a75c9a7bd6d336da27a03fc72c5ada3f56.nq.gz
│   ├── d3fdb7477b7364c38e2af240f729df35b9f39b80.nq.gz
│   ├── d59a8bed22cff72ca1dbd3543ea3ab4bf8c067d3.nq.gz
│   ├── d988b3ffdc2c791d0ab44c320e0299f5d12d758e.nq.gz
│   ├── e06ce1b7fc26ac39cfbe4cb49335296f8746bc85.nq.gz
│   ├── e858b9e48667dfd1eb008e7943f731196e570221.nq.gz
│   ├── f4efba810e18f9a61582a7a0828518abcaafa025.nq.gz
│   └── fe45ae08dca28cb48b9f8402589228b392f0c673.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 2d65066eeb06a5c9ff5184d8cebdf33662c67faf.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 48 files
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

[IST-DASLab/gptq](https://github.com/IST-DASLab/gptq)

---
*Parsed on 2026-10-17 by [repolex](https://repolex.ai)*
