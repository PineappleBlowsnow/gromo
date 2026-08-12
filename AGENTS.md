# Repository instructions

## Ownership

- This repository owns the reusable `gromo` Python library. Keep
  experiment-specific recipes, launchers, datasets, and result artifacts in
  their experiment repository; do not edit sibling repositories implicitly.

## Scope authorization and change review

- One clearly scoped user request authorizes the whole described in-repository
  batch. Do not request authorization again file by file. Full access and Codex
  `approval_policy` control command-time pauses, not acceptance of the resulting
  edits; repository instructions cannot override runtime security policy.
- Prefer reviewable text patches and preserve a focused Git diff. A supported
  Codex IDE workflow can review, keep, or undo edits in place. Binary changes,
  moves/renames, generated artifacts, and bulk formatting may not provide useful
  line-by-line review, so report those operations and paths explicitly.
- Do not commit unless asked.

## Verification

- Preserve the public growing-module interfaces and add or update focused tests
  for behavioral changes. Run the smallest relevant tests followed by the
  broader affected suite (matching CI: `coverage run -m unittest` after
  installing the `test` extra).
- Keep examples and tests self-contained. Changes required only by
  `experimental_grow` belong there unless they are genuinely reusable library
  behavior and are verified in this repository.
