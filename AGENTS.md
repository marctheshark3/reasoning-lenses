# Contributing

- Treat `skills/reasoning-lenses` as the distributable package. Keep the skill
  self-contained and its instructions focused on decisions that affect a review.
- Preserve the distinction between the original position, charitable
  interpretation, improved alternative, hypothetical objection and evidence.
- Keep examples synthetic and broadly applicable. Do not add credentials,
  transcripts, machine inventories or environment-specific operational policy.
- Keep evaluation prompts and behavioral criteria under `evals`, outside the
  installed package. Do not describe a maintainer's walkthrough as an independent
  trial or claim improved accuracy without comparative evidence.
- After instruction changes, use Skill Creator validation when available, run
  `git diff --check`, inspect local links, and review the evaluation scenarios.
- Keep the root and packaged MIT licenses identical.
