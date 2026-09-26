# Literature Landscape Review Skill

[中文说明](README.zh-CN.md)

An auditable literature-research skill for Codex and compatible agent workflows. It is designed to reduce missed prior work—especially recent work—and to replace binary novelty judgments with a defensible contribution analysis.

## Why this skill exists

AI-assisted literature reviews often fail in two predictable ways:

1. **Incomplete retrieval.** The assistant searches only the user's wording, misses renamed concepts or adjacent communities, and later discovers a highly similar paper.
2. **Poor novelty boundaries.** The assistant either rejects a direction because “someone has done something related,” or overstates novelty because an exact formulation was not found.

This skill makes those failure modes explicit. It asks the agent to search for the strongest counterexample to novelty, document what was and was not searched, compare against the closest prior work, and connect every claimed difference to measurable scientific or practical value.

## What it changes

### Coverage becomes auditable

The workflow uses three retrieval lanes:

- **Canonical:** surveys, seminal papers, taxonomies, and standard benchmarks.
- **Recent:** current and recent-year papers, preprints, proceedings, accepted-paper lists, and active research groups when appropriate.
- **Adversarial neighbor:** differently named or cross-disciplinary work most likely to invalidate the novelty claim.

It expands seeds through backward citations, forward citations, related-paper graphs, authors, labs, venues, historical terminology, and component-level searches. The result includes an explicit cutoff date, search boundaries, saturation evidence, and remaining blind spots.

### Novelty becomes a contribution boundary

The skill compares a proposal and its nearest papers across multiple dimensions:

- problem and target capability;
- setting and assumptions;
- mechanism or algorithm;
- data, supervision, feedback, and tools;
- theory or explanatory claim;
- evaluation and artifacts;
- robustness, safety, efficiency, and scale;
- intended scientific or practical outcome.

The conclusion is conditional rather than binary:

> The broad direction is established. The narrower contribution may be defensible if a concrete difference produces a consequential, measured result against the closest prior work.

## Expected output

A full review produced with this skill should contain:

- scope, search date, literature cutoff, sources, and inclusion policy;
- a taxonomy or chronological field map;
- verified representative papers and their actual contributions;
- a closest-prior-work comparison;
- established, weakly differentiating, defensible-if-validated, and speculative aspects;
- a minimal and publication-grade evidence plan;
- unresolved searches, blind spots, and calibrated confidence.

The skill does **not** promise a mathematically exhaustive review. It makes the search boundary visible and requires weaker conclusions when live search, database access, or verification is unavailable.

## Repository structure

```text
.
├── SKILL.md
├── agents/
│   └── openai.yaml
├── references/
│   ├── search-and-coverage.md
│   └── novelty-and-contribution.md
├── docs/
│   ├── design-rationale.md
│   └── prompt-examples.md
├── CONTRIBUTING.md
├── LICENSE
└── README.zh-CN.md
```

- [`SKILL.md`](SKILL.md) is the entry point and output contract.
- [`search-and-coverage.md`](references/search-and-coverage.md) defines query expansion, retrieval lanes, omission audits, and stopping criteria.
- [`novelty-and-contribution.md`](references/novelty-and-contribution.md) defines closest-work comparison and contribution-value analysis.

## Installation

### Codex skill directory

Clone the repository into your Codex skills directory:

```bash
git clone https://github.com/Imironman123/literature-landscape-review-skill.git "$CODEX_HOME/skills/literature-landscape-review"
```

On PowerShell:

```powershell
git clone https://github.com/Imironman123/literature-landscape-review-skill.git "$env:CODEX_HOME\skills\literature-landscape-review"
```

If `CODEX_HOME` is not configured, use the skill directory supported by your agent environment.

### Manual installation

Download the repository and place the folder containing `SKILL.md` under your skills directory. Keep `references/` and `agents/` beside `SKILL.md`; the entry point links to both reference protocols.

## Usage

Invoke the skill explicitly:

```text
Use $literature-landscape-review to map the literature on world-model-based
agents, find the closest prior work to my idea, and define the narrowest
defensible contribution with an evidence plan.
```

Or ask naturally when automatic skill discovery is enabled:

```text
Survey this research direction through the current date. Search for papers that
would most threaten the novelty of my proposal, compare the closest work, and
separate established ideas from contributions that remain defensible.
```

More task-specific prompts are in [`docs/prompt-examples.md`](docs/prompt-examples.md).

## Important operating assumptions

- Recent-work claims require live scholarly or web search. Without it, the agent must label conclusions provisional.
- A missing exact-keyword result is not evidence that no prior work exists.
- Search snippets and generated summaries are discovery aids, not primary evidence.
- Preprint and published versions should be merged rather than double-counted.
- A new combination, application, or benchmark is meaningful only if it produces a consequential and testable difference.

## Compatibility

The repository follows the Codex skill layout: YAML-frontmatter `SKILL.md`, optional UI metadata under `agents/`, and progressively disclosed reference files. The methodology can also be adapted to other agent systems that support reusable instruction packages.

## Contributing

Contributions are welcome, especially failure cases where the skill misses a close paper, confuses paper versions, overstates a contribution, or stops searching too early. See [`CONTRIBUTING.md`](CONTRIBUTING.md).

## License

[MIT](LICENSE)
