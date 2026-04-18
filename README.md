# Repolex Knowledge Graph of python-trio/trio-typing

RDF knowledge graph data for [python-trio/trio-typing](https://github.com/python-trio/trio-typing), parsed by [repolex](https://repolex.ai).

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
lexq download python-trio/trio-typing
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 886d729c5bb53b7ae432518b3fed6eed27c60e98
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 886d729c5bb53b7ae432518b3fed6eed27c60e98.nq.gz
│   └── repolex
│       └── 886d729c5bb53b7ae432518b3fed6eed27c60e98
│           └── chunk-001.nq.gz
├── blob
│   ├── 071b1a25abe96f612f55f40368b7f33e43b019e2.nq.gz
│   ├── 0dac61a6880632755e17abe7cd23cf6e79bb7537.nq.gz
│   ├── 104c402ebf17ef55f9cdca2114f0a4449f6dd039.nq.gz
│   ├── 10d2eaedb1c5d01560434efc166b1187e1cca2dc.nq.gz
│   ├── 18e13053ffaa425ad53a1f477b0d04eccf96df0c.nq.gz
│   ├── 393deb4e98f84814c557f1190fdef5aa0bce356c.nq.gz
│   ├── 4995b18418dbb1f817a8a22b17b0ab7233bba35d.nq.gz
│   ├── 4b7602e6723a3df2486f95126caa42cb8a641eb6.nq.gz
│   ├── 51f3442917839f8e0f0cccb52b3c10968ad0779e.nq.gz
│   ├── 54049ef94abf207ac32fce7d743061317862df3b.nq.gz
│   ├── 555e03c6e87b38372bf775c631daea83ab8beb1f.nq.gz
│   ├── 570df91153a581ba2a56cb044634cff10000959a.nq.gz
│   ├── 64264545399c85b8756dcbe4549d60d4308e5179.nq.gz
│   ├── 7bf9b761f7debc2e7d476750b80d29fe4f5dde52.nq.gz
│   ├── 7dc0747d6485172e06407ac93e081cbe3ff18e20.nq.gz
│   ├── 80ed00e67216adca089a7a4466116944d59b920f.nq.gz
│   ├── 8bc335e01944f920aef91696deab3a4e64b92987.nq.gz
│   ├── b6d895535e24c2ea594cfaca9cb3e027d708fe76.nq.gz
│   ├── b7f2434b084b520967d03c0d0f89f7980f362f9b.nq.gz
│   ├── b8bb97185926d7daed314609753173945ed4ff1a.nq.gz
│   ├── bebfb75fbef38be9588871522322d601bcde631a.nq.gz
│   ├── bfeb3517fef9fd240d5bc82dea4da016836828e6.nq.gz
│   ├── c0551931251e70245b3c15f2dd99567ec4f876df.nq.gz
│   ├── c60cf909b4d381f7d466712d8cdb12bdb9d0dd98.nq.gz
│   ├── ca88b1d5cccc75afaa72f88e2d270ad71541d798.nq.gz
│   ├── d636075eac87503b60f01ba2f3497058923417ab.nq.gz
│   ├── d645695673349e3947e8e5ae42332d0ac3164cd7.nq.gz
│   ├── e00bf1132a8e388d0cdc0f932627ee2fd11ca3ee.nq.gz
│   ├── e45f52e14ca122d36e485d846aa399244e5b64f4.nq.gz
│   ├── e57df2156bd00b136b7d20798a8a1a5d135ede97.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e81662ba048090a9fa4af9670c2dc2757abe1b91.nq.gz
│   ├── eb9575ef18469d6a7d195708d627227bf1f1b92b.nq.gz
│   ├── ecc04e945d139ee45d73ccb69d933df8b734dc9f.nq.gz
│   ├── f38c5167733eb2fd1cb677450f876788a4aa603e.nq.gz
│   └── fa0c00128e27121df58722614eb1cd9f036e2bb3.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 886d729c5bb53b7ae432518b3fed6eed27c60e98.nq.gz
├── filetree
│   └── 886d729c5bb53b7ae432518b3fed6eed27c60e98.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 46 files
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

[python-trio/trio-typing](https://github.com/python-trio/trio-typing)

---
*Parsed on 2026-04-18 by [repolex](https://repolex.ai)*
