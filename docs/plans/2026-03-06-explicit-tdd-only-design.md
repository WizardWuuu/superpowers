# Explicit TDD Only Design

**Goal:** Keep `test-driven-development` available, but stop it from activating automatically during normal implementation work.

## Decision

Adopt an opt-in TDD model:

- `test-driven-development` only applies when the user explicitly asks for TDD, test-first development, or red-green-refactor.
- Generic feature, bugfix, and refactoring requests must not trigger TDD automatically.
- Planning, execution, debugging, and verification skills should default to risk-appropriate verification instead of mandatory test-first steps.

## Scope

- Update the `test-driven-development` skill trigger and usage guidance.
- Remove default TDD requirements from planning and execution workflows.
- Replace TDD-specific debugging and completion guidance with generic reproducibility and verification guidance.
- Update top-level documentation and triggering tests to match the new behavior.

## Non-Goals

- Do not remove the TDD skill.
- Do not weaken verification requirements in general.
- Do not rewrite historical design documents under `docs/plans/`.

## Expected Behavior After Change

- Asking to implement a feature should not automatically invoke TDD.
- Asking to fix a bug should not automatically force failing-test-first workflow.
- Asking explicitly for "TDD", "test-first", or "red-green-refactor" should still invoke the TDD skill.
- Skills may still recommend tests when they are the right verification mechanism, but not as a mandatory default.
