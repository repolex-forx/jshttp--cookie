# Repolex Knowledge Graph of jshttp/cookie

RDF knowledge graph data for [jshttp/cookie](https://github.com/jshttp/cookie), parsed by [repolex](https://repolex.ai).

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
lexq download jshttp/cookie
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 1b89eec4e33256ac31962f4c0d6e711fff478803
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 1b89eec4e33256ac31962f4c0d6e711fff478803.nq.gz
│   └── repolex
│       └── 1b89eec4e33256ac31962f4c0d6e711fff478803
│           └── chunk-001.nq.gz
├── blob
│   ├── 053473708cc4d6c461a2fc7f478e086cca9810e1.nq.gz
│   ├── 058b6b4efa3f45896ae691f2558a2a1aca05bebd.nq.gz
│   ├── 060ac68db751a7d94be63a760360f01c16611e79.nq.gz
│   ├── 0e980d5849f30e97d43161214575c634df4600ee.nq.gz
│   ├── 10f0dd811cebfa673582c3a38971503117a0e3fb.nq.gz
│   ├── 12ae878558c47e8fbd602c7f768c2aa1bde516e8.nq.gz
│   ├── 24ec0132156fe93de3d6ad827b16872d6db7ad22.nq.gz
│   ├── 30fd59a6d6c5d749c1d8a59b013ba399dc547e45.nq.gz
│   ├── 4b7a898cad3f9b78adee3e71a33a2470376ca2d0.nq.gz
│   ├── 4fe35d2812f4f5bb1333908e91eb8d57c573238a.nq.gz
│   ├── 74b68eda6f67b41b8f2fff03c36611d7d84f0594.nq.gz
│   ├── 7da7acd684c7bd0197c72d2578fe92c57b3f2788.nq.gz
│   ├── 86188b5720a1face6e4656a98a374082fb83affc.nq.gz
│   ├── 92a56ead585ef0005d03f842231f333810ff5c7f.nq.gz
│   ├── 9dd124f7ae4d1e17e1721580e449b510ce22ebd5.nq.gz
│   ├── b9581759f68a94bbe564d9169965bf474c9de115.nq.gz
│   ├── c604e5332801ddf34c8ca9427ad0abab8390ffd2.nq.gz
│   ├── cdb36c1b4662559d2880d7a1ae9e65ca7497f47e.nq.gz
│   ├── cf740a476715e860f9d446bd04b5d9d5046ff73c.nq.gz
│   ├── d96c3b42bcd40698f787d9004d38280fb011a0df.nq.gz
│   ├── e1eb11a6492d124181498ae695ec45d3dc575cf7.nq.gz
│   ├── e73d59343eea6224ff5acbb5144fc262eb769634.nq.gz
│   └── ef26e8343e840a56c4645b9f7003f4f6acfb6202.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 1b89eec4e33256ac31962f4c0d6e711fff478803.nq.gz
├── filetree
│   └── 1b89eec4e33256ac31962f4c0d6e711fff478803.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 33 files
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

[jshttp/cookie](https://github.com/jshttp/cookie)

---
*Parsed on 2026-04-10 by [repolex](https://repolex.ai)*
