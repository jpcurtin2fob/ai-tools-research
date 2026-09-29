# AI / ML Tools Research

Shared research notes on tools for building, deploying, and operating ML and
generative-AI workloads on **AWS** (Amazon SageMaker AI and Amazon Bedrock).

Every write-up is plain Markdown, reviewed through pull requests, and follows a
standard template so tools can be compared side by side.

## Layout

| Folder | What goes there |
|---|---|
| [`templates/`](templates/) | Templates for tool evaluations, comparisons, and decision records |
| [`landscape/`](landscape/) | The big picture: where each tool fits in the ML lifecycle |
| [`tools/`](tools/) | One file per tool (e.g. `tools/mlflow.md`) |
| [`comparisons/`](comparisons/) | Head-to-head comparisons of overlapping options |
| [`decisions/`](decisions/) | Architecture Decision Records (ADRs): what we chose and why |
| [`spikes/`](spikes/) | Small, runnable proofs of concept backing up the write-ups |

## Tool index

| Tool | Category | Status | Owner | Last reviewed |
|---|---|---|---|---|
| [Pydantic](tools/pydantic.md) | Data validation / LLM structured output | Not started | | |
| [MLflow](tools/mlflow.md) | Experiment tracking / model registry | Not started | | |
| [Evidently](tools/evidently.md) | Data & model monitoring | Not started | | |

**Status values:** Not started · Researching · Piloting · Adopted · Rejected

## How to contribute

1. Create a branch: `research/<tool-name>`.
2. Copy [`templates/tool-evaluation.md`](templates/tool-evaluation.md) to `tools/<tool-name>.md`
   (lowercase, hyphenated), or fill in the existing stub.
3. Fill in every section. If something doesn't apply, say so rather than deleting it.
4. Add or update the row in the **Tool index** above.
5. Open a pull request. Changes to `decisions/` need approval from at least two reviewers.

## Ground rules

- **Cite sources.** Every write-up ends with a Sources section linking official docs.
- **Date everything.** These tools change fast. Record the version evaluated and the
  "Last reviewed" date. Anything older than 6 months should be re-checked before relying on it.
- **Prefer evidence over opinion.** Link to a spike in `spikes/` when you can.
- **AI-assisted drafts are welcome, but a human verifies them.** Check every
  version-specific claim, price, and AWS feature against the official docs before merging.

## Using Claude with this repo

[`CLAUDE.md`](CLAUDE.md) gives Claude the context for this project (our stack,
conventions, and templates). In Claude Code, run:

```
/research-tool <tool name>
```

to draft a new evaluation from the template. Treat the result as a first draft to verify.
