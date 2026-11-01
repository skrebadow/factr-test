# Behavioral test design — MAP capability

Design from the available input. Do not require a formal source hierarchy or runtime evidence to produce a provisional test.

Begin by distinguishing what is already supported from what is missing for a concrete procedure and for automation, following the entry skill's opening assessment. Address those gaps before presenting cases; do not hide them in a closing assumptions list.

## Assertions and conditions

Identify the independently challengeable commitments, retaining concrete constraints and their source support. Separate a required rule from a proposed edge case. A source may support several assertions; a criterion count does not dictate a test count.

For each relevant assertion identify:
- Responsible subject and scoped trigger/input/state.
- Expected behavior and distinguishable outcome.
- Contrary observation that would contradict that behavior.
- An observation boundary capable of distinguishing those outcomes.
- Material assumptions or open interpretation choices.

Unknown precision stays unknown. Do not manufacture a deadline for an eventual outcome. Absence can be a falsifier only when the source establishes the observation conditions/window; otherwise a missing observation may be inconclusive.

## Choose useful cases

Select conditions and data that discriminate compliance from failure. Use boundaries, invalid inputs, permissions, state transitions, and interactions when grounded in the behavior. Avoid generic happy/negative/edge counts or a default end-to-end requirement.

Keep setup, stimulus, and expected results distinct. An assertion about the system's decision belongs to the result, not an action that assumes it occurred. Make failure attributable: a missing setup fixture is not automatically a product rejection defect.

Use supplied schema/data constraints for fixtures. Label invented representative values as illustrative; their shape or target acceptance is not discovered. A schema alone does not establish that a runtime interface accepts the example.

Several cases may challenge one assertion under different conditions. Several assertions may share a scenario when separate observations identify which commitment failed. Do not duplicate tests solely because multiple requirements support the same behavior.

## Evidence and observation

Select the smallest sufficient boundary: inspection, analysis, unit or integration check, UI interaction, device measurement, demonstration, or operational observation may be appropriate.

A related log, accepted request, queue entry, configuration record, or successful setup does not establish a downstream outcome without a supported relationship. For message rejection, distinguish sender acceptance, receiver disposition, and downstream processing. For retained settings, distinguish stored configuration from effective behavior.

When an observation surface or correlation mechanism is unknown, specify the needed evidence and use [discovery.md](discovery.md) if locating it is needed for the user's result. Continue with a draft when access is unavailable.

## Output

When a test procedure is requested, make it possible for another tester to perform the test: identify the target, access and initial state, concrete inputs, ordered setup and stimulus actions, observation method and expected result, evidence to capture, and necessary reset/cleanup. Include commands or interface details only when supported. Mark missing instructions at the affected step and explain what would resolve them; a generic "submit the input" or "verify rejection" is incomplete when the actual submission or observation method is unknown.

Separate procedure completeness from automation readiness. Identify reusable Gherkin steps and supported bindings when useful, then the additional interfaces, fixtures, dependencies, and configuration needed to automate them. A procedure may be usable manually without an automation binding. Do not label a provisional procedure runnable merely because its expected behavior is clear.

A lean case can retain:
- ID/title and source/assertion reference.
- Purpose, conditions, and required inputs.
- Causal actions or inspection approach.
- Observable expected result and failure indicators.
- Evidence needs and material assumptions/open gaps.

A step/data/expected-result table is useful for a workflow; it is not mandatory. Given/When/Then may organize a case without requiring a separate Gherkin file. Do not force a universal metadata ledger.

For existing-test review, identify which contrary observations the tests can detect, their relevant conditions, and uncovered commitments within reviewed scope. A test/source link or passing run does not establish complete coverage. Compare meaningful scope before reporting gaps or duplication.
