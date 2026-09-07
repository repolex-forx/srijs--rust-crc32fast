# Repolex Knowledge Graph of srijs/rust-crc32fast

RDF knowledge graph data for [srijs/rust-crc32fast](https://github.com/srijs/rust-crc32fast), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [lexq](https://github.com/repolex-ai/lexq) query tool using [uv](https://docs.astral.sh/uv/getting-started/installation/).

If you have uv installed, just copy/paste this into your terminal:

```bash
uv tool install git+https://github.com/repolex-ai/lexq
```

This installs lexq onto your system, in your user context. Verify the install:

```bash
lexq --help
```

**lexq is designed to be used primarily by LLMs in a terminal.** Start up your favorite LLM and ask it to use the lexq tool. It's that easy!

To load this repo's data:

```bash
lexq download srijs/rust-crc32fast
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── a150f65ce810793293d5c9dd815f4510eb6d8e4c
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── a150f65ce810793293d5c9dd815f4510eb6d8e4c.nq.gz
│   └── repolex
│       └── a150f65ce810793293d5c9dd815f4510eb6d8e4c
│           └── chunk-001.nq.gz
├── blob
│   ├── 0c286a3ab986d81a37b4e9ee550d764996f8028c.nq.gz
│   ├── 0e0dde2eeb4b3e9dec1ae59556d4b19c4305fdcc.nq.gz
│   ├── 1a45eee7760d240bfa8ac1989088e0349169f264.nq.gz
│   ├── 2f246e63b909862cc448ea94fd9c4d7e04f56bd5.nq.gz
│   ├── 2f62d93675848c0078bef841bea59b94cb86e8e9.nq.gz
│   ├── 3a5b203f72f784dd023db46440ad58db427ae8ae.nq.gz
│   ├── 472088efa94f4622602301af15e37bccf9d27374.nq.gz
│   ├── 78b89c3212fefceba7ffc4ccdc6c35e3e3d92289.nq.gz
│   ├── 7a1a63c08b127958ccaef557316722fa3762c793.nq.gz
│   ├── 7d5914e021a56c717e840dd8f8c11bce090e2ac7.nq.gz
│   ├── 7dc42de8a3cf18e1a9d3ad56b4a82675b5becd4c.nq.gz
│   ├── 7f8a8708137f73c3d05cc7e2465b7e07105751fa.nq.gz
│   ├── 8f47c45738cece8fb9bfd1ed02165e4ba2787ac1.nq.gz
│   ├── 8f71f43fee3f78649d238238cbde51e6d7055c82.nq.gz
│   ├── a7096c174652be6431eb1c9b0eb2f450aaef8dd8.nq.gz
│   ├── afff984f8e38d15b41b8941dd28d69bab593c670.nq.gz
│   ├── bf2ddc138af96af4224c6e98968b14c7fa836ac0.nq.gz
│   ├── ca06f4fada17894600a1731b3ba34df899ebe0e6.nq.gz
│   ├── e69f1cadd2be92ede15ee09db8aed24f347bc6b7.nq.gz
│   └── f558267301a4865228ad777c3c1c127b50bc65cc.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── a150f65ce810793293d5c9dd815f4510eb6d8e4c.nq.gz
├── filetree
│   └── a150f65ce810793293d5c9dd815f4510eb6d8e4c.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 30 files
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

## Source repository

[srijs/rust-crc32fast](https://github.com/srijs/rust-crc32fast)

---
*Parsed on 2026-09-07 by [repolex](https://repolex.ai)*
