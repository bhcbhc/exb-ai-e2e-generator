---
name: e2e-test-generator
description: Generate maintainable end-to-end tests for application user flows from requirements or existing behavior. Use when asked to create, add, or update E2E/browser tests.
---

# E2E Test Generator

Create focused end-to-end tests that verify user-visible application behavior.

## Workflow

1. Inspect the target repository before editing. Read its project manifest,
   test configuration, existing E2E tests, and relevant application code.
2. Identify the configured browser-testing framework, test locations, scripts,
   fixtures, authentication setup, and established style. Follow those
   conventions; do not introduce another framework or dependency.
3. Translate the request into concrete user flows and observable outcomes.
   Include important success and failure cases, but avoid duplicating existing
   coverage or expanding beyond the requested behavior.
4. Implement the smallest set of tests and any necessary test-only setup.
   Keep tests independent and deterministic; use existing fixtures and isolate
   or clean up any test data they create.
5. Prefer accessible, user-facing locators such as roles, labels, and
   placeholder or visible text. Avoid brittle selectors, fixed sleeps, and
   assertions against implementation details when a user-visible assertion is
   available.
6. Run the narrowest relevant existing test command. Do not invent commands or
   modify unrelated code to make the tests pass.
7. Summarize the files changed, the behavior covered, and the checks run.
   Clearly report any assumptions, missing setup, or tests that could not be
   run.

## Framework and missing information

- Use the framework already configured in the target repository, whether it is
  Playwright, Cypress, WebdriverIO, or another existing tool.
- If no E2E framework is configured, do not install one silently. Ask which
  framework to use, or propose a minimal option and wait for approval before
  adding dependencies.
- If the requested behavior or test setup is ambiguous in a way that affects
  correctness, ask a concise clarifying question. Otherwise, state reasonable
  assumptions and keep the tests scoped to the request.
