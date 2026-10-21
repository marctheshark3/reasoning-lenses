# Reasoning Lenses

A portable agent skill for strengthening ideas, challenging them fairly, and
deciding what to improve or test next.

Use it for proposals, arguments, plans, designs and code decisions that benefit
from deliberate scrutiny. It combines faithful interpretation, steelmanning,
adversarial challenge, collaborative improvement and identifying the assumptions
that would change a decision. Straw men are something to detect and correct.

The skill distinguishes the original proposal from an improved alternative,
keeps hypothetical claims separate from evidence, and avoids forced balance.
It adapts to constructive, adversarial or combined reviews.

## Install and use

Install the contents of [`skills/reasoning-lenses`](skills/reasoning-lenses) as a
folder named `reasoning-lenses` in your agent's supported skill discovery
directory. Retain its `SKILL.md`, `agents`, `references` and `LICENSE` files. The
package contains Markdown and YAML; it needs no executable runtime or external
service. The included UI metadata supports Codex. Other agents that read
`SKILL.md` may need their own discovery configuration.

Example requests:

```text
Use $reasoning-lenses to stress-test this architecture decision.

Use $reasoning-lenses constructively: help improve this plan while preserving
its offline-only requirement.

Use $reasoning-lenses to assess the strongest case and objection, suggest an
improved proposal, and identify the next test that could change our decision.
```

A combined review often returns **strongest case → strongest objection →
improved proposal → next test**. The skill does not require every lens when a
smaller assessment answers the request.

## Maintain and evaluate

Edit the packaged source in `skills/reasoning-lenses`. The
[worked examples and foundations](skills/reasoning-lenses/references/examples-and-foundations.md)
explain important distinctions. Separate [evaluation cases](evals/cases.json)
provide synthetic requests and behavioral criteria for future trials; do not
give the criteria to a model completing a blinded trial.

If Skill Creator is available, run its `quick_validate.py` on the skill folder.
Also run `git diff --check`, verify local links and package completeness, and
review the evaluation cases against the changed instructions. Structural checks
and a maintainer's scenario review do not establish improved reasoning accuracy
or constitute an independent model evaluation.

## License

[MIT](LICENSE). The package includes a copy of the license for standalone
distribution. Referenced publications retain their own rights.
