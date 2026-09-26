# Design rationale

## Problem 1: retrieval can look broad while remaining structurally incomplete

The most dangerous omissions are often not caused by too few results. They arise because every query shares the same vocabulary and assumptions. Searching more pages of the same result family does not repair that problem.

The skill therefore emphasizes **independent discovery paths**:

- lexical expansion using aliases, historical terms, broader and narrower tasks;
- structural expansion through backward and forward citations;
- social expansion through authors and labs;
- venue expansion through current programs and accepted-paper lists;
- conceptual expansion through mechanisms, expected outcomes, benchmarks, and adjacent disciplines.

It also separates canonical coverage, current coverage, and closest-prior-work coverage. Confidence can be high for one and moderate for another.

## Problem 2: novelty is not the absence of ancestry

Research contributions usually inherit an existing problem, method family, empirical observation, or theoretical foundation. Treating any related work as disqualifying suppresses legitimate contributions. Treating the lack of an exact match as novelty creates fragile claims.

The skill uses a contribution vector instead of a binary label. A meaningful difference may lie in formulation, assumptions, mechanism, evidence, operating regime, explanation, robustness, efficiency, or reusable artifact. That difference becomes a contribution only when it has a plausible mechanism and a consequential, testable outcome.

## Why search is adversarial

Ordinary helpfulness can produce confirmation bias: once an appealing research story emerges, the agent may retrieve papers that support it. The skill changes the objective to finding the strongest prior work against the proposed claim. Surviving that comparison produces a narrower but more credible contribution.

## Why the protocol does not promise exhaustive coverage

No practical search can guarantee access to every paper, patent, unpublished manuscript, renamed idea, or newly posted preprint. A claim of absolute completeness would itself be unreliable. The protocol instead requires:

- an explicit search date and literature cutoff;
- documented source and publication-status boundaries;
- query-family and citation-neighborhood expansion;
- saturation criteria;
- residual blind spots and confidence calibration.

The result is intended to be **decision-sufficient and auditable**, not metaphysically complete.

## Why a new idea still needs anchors

Lack of direct precedent is not automatic evidence of importance. Highly novel ideas should be grounded by:

1. an empirical or theoretical foundation;
2. a plausible mechanism;
3. a falsifiable, inexpensive bridge experiment.

This supports exploration without confusing novelty with value or feasibility.
