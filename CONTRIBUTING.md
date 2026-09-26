# Contributing

Contributions should improve observable research behavior rather than merely add more instructions.

## High-value contributions

- A real query where the skill missed a close or differently named paper.
- A case where preprint and published versions were double-counted.
- A novelty assessment that was too broad, too dismissive, or unsupported.
- A search protocol improvement that adds a genuinely independent discovery path.
- A clearer evidence test connecting a proposed difference to scientific or practical value.

## Proposing a change

Please include:

1. The original research request or a minimally anonymized equivalent.
2. The observed failure and why it matters.
3. The smallest instruction change that would correct the behavior.
4. A realistic test request showing the desired behavior.
5. Any tradeoff, such as extra search cost or a narrower trigger boundary.

Avoid adding generic advice, large lists of specific databases, or fixed step counts unless a demonstrated failure requires them. The skill should remain useful across research fields and search-tool configurations.

## Validation

Before submitting a change:

- Confirm that `SKILL.md` still has valid YAML frontmatter and the folder name matches the skill name.
- Check that every referenced file exists and is reachable from `SKILL.md`.
- Search for unfinished placeholders such as `TODO`.
- Test at least one landscape-review request and one novelty-stress-test request.
- Verify that unavailable live search leads to a provisional conclusion rather than a false completeness claim.

If you have the Codex skill-creator validator available, run its `quick_validate.py` against the repository root.
