# Repolex Knowledge Graph of asimov-modules/asimov-huggingface-module

RDF knowledge graph data for [asimov-modules/asimov-huggingface-module](https://github.com/asimov-modules/asimov-huggingface-module), parsed by [repolex](https://repolex.ai).

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
rlex download asimov-modules/asimov-huggingface-module
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── b4216159f8ced806e94f4856cca4d20fb644dc26
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── b4216159f8ced806e94f4856cca4d20fb644dc26.nq.gz
│   └── repolex
│       └── b4216159f8ced806e94f4856cca4d20fb644dc26
│           └── chunk-001.nq.gz
├── blob
│   ├── 062b676000d1b3475f1a99b633afa53368d65754.nq.gz
│   ├── 1d013ff92fa855fb03f148d15f9488c339392020.nq.gz
│   ├── 2391f73aa051d3804285ce744f2e9a1c7e08993d.nq.gz
│   ├── 3041bf28e48619a0c773c6840e3f734fd3d3ef27.nq.gz
│   ├── 5dc50bcc4043313cb30c4702b021d658692f3cd0.nq.gz
│   ├── 5f5cf896c81688e4360b37f1bcda92f7bc6f7423.nq.gz
│   ├── 75e3b65f99b29f48ab230e3eab3de8d0b7a9229f.nq.gz
│   ├── 77d6f4ca23711533e724789a0a0045eab28c5ea6.nq.gz
│   ├── af9908b08f4b33c32a0080af73f53bc0fa0cdce4.nq.gz
│   ├── c8fc03c6d7f073d1fe862cac36cff1a3ae619edd.nq.gz
│   ├── cf42f6893594e2f8be2b722de51123d65e4d61c4.nq.gz
│   ├── d33b3537869750b102370a8011c906be6b172e40.nq.gz
│   ├── e3e57a8ce4ccbf74759a6df8fa4a3980ff1c9209.nq.gz
│   ├── e75b77fcde0cf8341f8733165c220611440b3860.nq.gz
│   └── efb98088164f5786b17e83ed384971fc3c74f93c.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── b4216159f8ced806e94f4856cca4d20fb644dc26.nq.gz
├── filetree
│   └── b4216159f8ced806e94f4856cca4d20fb644dc26.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 25 files
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

[asimov-modules/asimov-huggingface-module](https://github.com/asimov-modules/asimov-huggingface-module)

---
*Parsed on 2026-09-28 by [repolex](https://repolex.ai)*
