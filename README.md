# exb-ai-e2e-generator

An agent skill for generating end-to-end (E2E) tests from feature requirements,
user stories, or existing application behavior.

## Install

Copy `.github/skills/e2e-test-generator` into the `.github/skills` directory of
the repository where you want to use the skill. GitHub Copilot can then load it
when a request matches its description.

## Use

Ask Copilot to generate E2E tests for a feature or user flow. For example:

> Generate E2E tests for signing in, including invalid credentials and a
> successful sign-in.

The skill inspects the project first, uses its configured test framework and
existing conventions, and adds focused tests for the requested behavior. It
does not add a new test framework or dependency without being asked.
