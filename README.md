# progression-spec

Research and planning space for a **spec-driven AI development framework** for a mobile app mirroring the scope of `juloberno/progression`.

## Goal

Define a high-level, user-perspective-first specification approach that a GitHub agent can execute reliably.

## Candidate frameworks

| Option | What it looks like | User-perspective modeling | Mobile fit | Agent fit |
| --- | --- | --- | --- | --- |
| **BDD / Spec by Example (Gherkin + Cucumber + Appium/Maestro)** | Features in `Given/When/Then`, tied to acceptance tests | Excellent (direct user journeys) | Strong | Strong |
| **Model-Based Testing (state model + generated paths)** | State diagrams and transitions generate tests | Good (if journeys are mapped to states) | Strong for complex flows | Medium |
| **User Story Mapping + executable acceptance checks** | Story map + acceptance criteria converted to checks | Excellent for product discovery | Medium | Medium |

## Recommended starting point

Start with **BDD / Spec by Example**:

1. Capture user journeys as Gherkin features.
2. Keep scenarios at product language level (user outcomes, not implementation).
3. Bind scenarios to mobile checks (Appium or Maestro).
4. Let the GitHub agent iterate from specs -> implementation -> validation.

Why this first:
- Best match for “high-level, user perspective” modeling.
- Straightforward for AI agents to parse and execute.
- Produces living documentation plus executable acceptance criteria.

## Decision checkpoint

If we agree with the recommendation, the next step is to commit to:
- Mobile runner: **Maestro** or **Appium**
- Feature structure and naming conventions
- Definition of Done per scenario (acceptance + non-functional checks)