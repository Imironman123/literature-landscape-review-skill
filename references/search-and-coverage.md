# Search and Coverage Protocol

Use this protocol when the task requires a literature landscape, recent-work coverage, or confidence that important neighboring work has not been missed.

## Define a coverage contract

Before searching, write down the effective boundary:

- Research questions and decisions the review must support.
- Search date and exact literature cutoff. Interpret “latest” as through the current date, not merely the current year.
- Relevant disciplines and neighboring communities.
- Included statuses: peer-reviewed papers, accepted or online-first papers, preprints, workshop papers, theses, datasets, benchmarks, or patents as appropriate.
- Language and access limitations.

The contract is not a claim of exhaustiveness. It makes omissions visible and conclusions revisable.

## Build a query matrix

Expand the concept along independent axes, then combine terms across axes:

| Axis | Examples of what to derive |
|---|---|
| Problem or object | formal name, colloquial name, predecessor term, broader and narrower task |
| Mechanism | model family, algorithm, architecture, learning signal, planning or inference method |
| Setting | embodied, multi-agent, open-world, partial observability, long horizon, online, offline |
| Constraint or property | causality, memory, compositionality, robustness, safety, efficiency, generalization |
| Evidence | benchmark, dataset, simulator, theorem, ablation, human study, deployment |
| Relationship terms | survey, benchmark, taxonomy, comparison, review, “related work”, failure mode |

Include spelling variants, acronyms, renamed concepts, and terms used by adjacent communities. Search important component pairs even when the full idea has no established name.

## Search in three lanes

### 1. Canonical lane

Find surveys, taxonomies, seminal papers, widely used benchmarks, and highly cited turning points. Use these to learn field vocabulary and locate historical roots, not as a substitute for recent search.

### 2. Recent lane

Search the current year and recent preceding years explicitly. Include preprints, accepted-paper lists, proceedings, and online-first publications when appropriate. For fast-moving topics, inspect major venue programs and active author or lab publication pages in addition to index searches.

Record a search cutoff date. Re-run freshness-sensitive queries near final delivery if the investigation spans multiple days.

### 3. Adversarial-neighbor lane

Search for work most likely to invalidate the novelty story:

- Same problem under a different method name.
- Same mechanism applied to a neighboring problem.
- Same claimed benefit evaluated in a different setting.
- A component-level paper that already contains the proposed technical insight.
- Work from another discipline using different terminology.
- Negative results, replications, benchmarks, or surveys that challenge the premise.

Phrase some queries around the expected result or capability rather than the proposed method name.

## Use multiple discovery paths

Choose sources appropriate to the field. Useful paths include scholarly search engines and indexes, field-specific archives, publisher or venue pages, citation graphs, and author pages. Do not treat several frontends backed by the same index as independent evidence.

From each strong seed paper, perform:

1. Backward citation search for foundations and inherited assumptions.
2. Forward citation search for extensions, corrections, and competing results.
3. Similar-paper or bibliographic-coupling search for nearest neighbors.
4. Author and lab search for renamed, follow-up, or concurrent work.
5. Venue scan for papers that use the field's current language.

Follow at least two independent discovery paths for every central subquestion. “Independent” means different query logic, citation direction, community, or source corpus—not only a different website.

## Maintain an evidence ledger

For every paper relied on materially, capture:

- Verified title, authors, year, venue or publication status.
- DOI, arXiv identifier, or stable landing-page URL.
- Version relationship: preprint, workshop, conference, journal extension, or duplicate.
- Research question, method, setting, data or feedback, and evaluation.
- What the paper actually demonstrates and what it does not.
- Relevance to the landscape or proposed contribution.
- Discovery path and any verification uncertainty.

Prefer the primary paper and official metadata. Use secondary sources to discover papers or understand context, then verify against the original.

## Detect and repair likely omissions

Before concluding, run a missed-prior-art audit:

- Translate the central idea into broader, narrower, older, and outcome-based wording.
- Remove one component at a time and search the remaining core mechanism.
- Search each pair of components in a multi-part proposal.
- Search major baselines and benchmarks plus the proposed capability.
- Inspect terminology used in the closest papers and repeat the search with their vocabulary.
- Search adjacent communities and venues.
- Look for very recent preprints and accepted-but-not-yet-proceedings papers.
- Check whether apparent separate papers are versions of the same work.

If results are unexpectedly sparse, broaden vocabulary and communities before interpreting scarcity as novelty.

## Saturation and stopping

Stop when the review is decision-sufficient, not when search becomes tiring. A reasonable saturation claim requires all of the following when relevant:

- Each central subquestion has been searched through multiple query families and at least two discovery paths.
- Canonical seeds, their forward and backward neighborhoods, and the closest current papers have been inspected.
- Recent top venues or equivalent high-signal sources have been checked for the applicable cutoff.
- Two successive expansion rounds yield no new major category and no paper that materially changes the closest-work comparison.
- Remaining gaps are caused by an explicit boundary such as paywalls, unavailable databases, language, or time—not an unexamined query family.

If these conditions are not met, call the result a rapid scan or preliminary map rather than a comprehensive review.

## Report coverage honestly

Summarize:

- Search date and cutoff.
- Sources or surfaces searched.
- Main query families, rather than an unreadable dump of every query.
- Inclusion and exclusion choices.
- Saturation evidence.
- Access restrictions and residual blind spots.
- Confidence in canonical coverage, recent coverage, and closest-prior-work coverage separately.

Use confidence labels only with reasons. For example, recent-work confidence may be moderate even when canonical coverage is strong.
