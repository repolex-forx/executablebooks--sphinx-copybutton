# Repolex Knowledge Graph of executablebooks/sphinx-copybutton

RDF knowledge graph data for [executablebooks/sphinx-copybutton](https://github.com/executablebooks/sphinx-copybutton), parsed by [repolex](https://repolex.ai).

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
rlex download executablebooks/sphinx-copybutton
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── ef430062a3b7b2046f0283dcc42ee696e5878fd9
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── ef430062a3b7b2046f0283dcc42ee696e5878fd9
│           └── chunk-001.nq.gz
├── blob
│   ├── 0c9e0fc1447e98b7f63ae8c9eb552c2af7b83f45.nq.gz
│   ├── 0dbae47a76a4e7bf55b8871ee7b7d8cea3b0af1d.nq.gz
│   ├── 1f80aea974f79cfd22e6b8303745a0ce0f10b101.nq.gz
│   ├── 27873932770653045a5e7a180f00e1bc45eb4339.nq.gz
│   ├── 28d15ef89e5ad82504d9c804734385f4333b4db5.nq.gz
│   ├── 44cc723b807d832f9634e6a9014cc9c9f70998fc.nq.gz
│   ├── 48be52c29e6712c016abac8f945956e00ddbe9fa.nq.gz
│   ├── 4c90285ff663f2cae8ea2003e8e1c5842d080f70.nq.gz
│   ├── 4f44e01962e618d007a4b78f4c34cb9e3645b45b.nq.gz
│   ├── 5c42436da61ae13e918fe9d4b6efe0e3fe0f8d0e.nq.gz
│   ├── 66efc0fecd1554e6e4681fcb149692591f388bf2.nq.gz
│   ├── 6e0e4adea839afa34a6dea5c94e2b75e5eaa612c.nq.gz
│   ├── 6fa6fc7d0bf4be84cb0f6feb460d98a9ea9ff51f.nq.gz
│   ├── 714e5e229dc23c2043c5603c68c6d1caea20a012.nq.gz
│   ├── 7fe7b1557da159c8edbd8471dd3d7e7f8d18ee31.nq.gz
│   ├── 8dac2b43c314071a89ade49b0af090d89af9c697.nq.gz
│   ├── 92fad4b5c0b766702548d26ab2be2832e19ad4da.nq.gz
│   ├── 93613cd3aca530c78b043e1be0e12389663ad0a6.nq.gz
│   ├── 953e7f34db5be04c55cbf71c6bbe4fcce56e9587.nq.gz
│   ├── 9c074dae5283fb4a5371c2492cd376043117f071.nq.gz
│   ├── a74e7a88b39645f6acf318a47f4f7f67678eb13e.nq.gz
│   ├── b888a20dfb9aa7c666a6b8dbe4a5f505fbfcfb14.nq.gz
│   ├── be9994914b6724d1095ea8353148ef2770073a6b.nq.gz
│   ├── cf5a036727ebef7097dbbcbc523c9e833427f290.nq.gz
│   ├── dab6ba48f3dcb26eae65920afb84113b1ebb141f.nq.gz
│   ├── dbe1aaad79cd1f835c8fbb304d255e19a3b39512.nq.gz
│   ├── dda9865ad01e8f6ecebfc69f0889c81050a594f0.nq.gz
│   ├── e7513363b324b2a105435c567da089af8b75736a.nq.gz
│   ├── e935a4ec385839f439376ef39441be0574a048fb.nq.gz
│   ├── ec91f2096ba5f5d367e0108b518a9de4a8f36d0f.nq.gz
│   ├── f1916ec7d1bb993b7909cd57cef0446d922982ff.nq.gz
│   ├── f2158d55444443beb42c65882e8489309bc14107.nq.gz
│   ├── f3d1febc9b69e6db87eba61726351f7718ab2e64.nq.gz
│   ├── f564d0295ef14a20d28d67d7633f9875a0c092bd.nq.gz
│   ├── f8332005db2d3a7ff11e30039110aa164305cc3e.nq.gz
│   └── faa98eef46517c76aa6489cb3ccb23cce9efc809.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── ef430062a3b7b2046f0283dcc42ee696e5878fd9.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 44 files
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

[executablebooks/sphinx-copybutton](https://github.com/executablebooks/sphinx-copybutton)

---
*Parsed on 2026-10-12 by [repolex](https://repolex.ai)*
