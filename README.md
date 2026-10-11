# Repolex Knowledge Graph of pytest-dev/pytest-incremental

RDF knowledge graph data for [pytest-dev/pytest-incremental](https://github.com/pytest-dev/pytest-incremental), parsed by [repolex](https://repolex.ai).

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
rlex download pytest-dev/pytest-incremental
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 373cf8224ae2c86ace11ed28507fd7f4ae052902
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 373cf8224ae2c86ace11ed28507fd7f4ae052902
│           └── chunk-001.nq.gz
├── blob
│   ├── 1251ea93bc48a625199ad748c04e68c99235681e.nq.gz
│   ├── 1c18d04ad1dbc296b568ac5632705d6b4d782dc7.nq.gz
│   ├── 1ca231c65bf751922a09028c54e43c89d16e34c7.nq.gz
│   ├── 1fe5f2d9295611a69a8dcbc514d5417152382ae0.nq.gz
│   ├── 28646c54815a4fcce52642a0fd015cbdf8ab134d.nq.gz
│   ├── 2900b44565fd57d85a6460aae3fbaab0eb83eb24.nq.gz
│   ├── 5299586f0ac13e7eec3c8d6f3c89a80177286ee3.nq.gz
│   ├── 5a802f6022643d945f9bd7fb687571ce77badf1b.nq.gz
│   ├── 606eb92760c364b7cceac978e44a9012561e6118.nq.gz
│   ├── 634f450142c57524bceae360b81be21f6f1ab9d4.nq.gz
│   ├── 665c1b2eeb346e80e231b0cb8ff057a9244d60e5.nq.gz
│   ├── 6717c8d116d47409697a3eeebf3e49c7d7c8893e.nq.gz
│   ├── 6c0686c4bc11fb40205e4cae9b5c5be179e18beb.nq.gz
│   ├── 6cc781ebea9d13e884fd543ce89ae1534ed1de03.nq.gz
│   ├── 72ce00eb292a18ae822241041db9153fd826afd0.nq.gz
│   ├── 76ca2631d3b20d415a9cbc5967b3549912e48fdd.nq.gz
│   ├── 83766cc26487e4ce69357d96bea1f78c40aa108e.nq.gz
│   ├── 8f92bc92eb9d027e3851ec58047cd76a65efac53.nq.gz
│   ├── 9140327592321121884ccb6b692bf9acc0c2062f.nq.gz
│   ├── 93dd00416f7f9ddad9da49060c59e4241176cb5b.nq.gz
│   ├── 9e579bec5520e9279bd1d68582e44b65ea4922fc.nq.gz
│   ├── be81517de386ed0f24c01dc7b743e01ebfa7fa48.nq.gz
│   ├── d1b130110c4d70ad453314130261305226f5deaa.nq.gz
│   ├── d5d2c6904c0600338a14966196777a1b45e2a694.nq.gz
│   ├── edd51b785734963ec7093309badbb72359c408ed.nq.gz
│   ├── ef87708ae702cf8f9e1fe003d49be4bf41b3b1fd.nq.gz
│   ├── f466e16d3d85f6042b324b9fe1cb5939ab51a57c.nq.gz
│   ├── f6ddfd88f756cedf357d0382f10a9f3e0ae3cab6.nq.gz
│   └── f714fbbb45a34a4b979b0537abc45f31400b0caa.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 373cf8224ae2c86ace11ed28507fd7f4ae052902.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 37 files
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

[pytest-dev/pytest-incremental](https://github.com/pytest-dev/pytest-incremental)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
