---
name: factr-test
description: Identify gaps for concrete test procedures and automation, design falsifiable tests, discover evidence and bindings, and render Gherkin or supported automation. Use for behavioral test design and FACTR Test requests.
---

# FACTR Test

Version 0.1.0. Apply FACTR Core's methodology to test design, targeted discovery, and rendering. MAP and RENDER are capabilities, not required stages.

## Apply Core within Test's scope

Read [the bundled Core contract](references/core/contract.md) once when applying this skill; reuse unchanged context. It owns assertion anatomy, bounded inference, support, evidence, evaluation, and formal acceptance. Core's broader capabilities supply reasoning principles; Test's deliverables are test designs, discovery findings, scenarios, and supported automation.

Use supplied descriptions, requirements, criteria, assertions, existing tests, code, and observations directly. No approved FACT Set, Understanding Map, Agile output, or HARDEN artifact is required. FACTR Test has its own inputs and workflow; do not invoke Agile or establish a handoff to it. Installation alone does not start work or authorize external actions.

## Start with procedure and automation gaps

For test design, procedure, or automation requests, first assess the supplied context and lead with what is missing to write an actionable test procedure and what automation would additionally need. Separate missing behavioral decisions, procedure details, and automation bindings/dependencies. Use [discovery.md](references/discovery.md) to resolve material gaps when inspection is useful; this opening assessment does not require a separate discovery artifact or a full environment inventory.

For each material gap, explain the affected setup, action, observation, or binding; why the gap matters; and the specific information or inspection that would resolve it. Reuse supplied answers and supported findings. Ask focused questions for consequential choices while continuing supported work. If the relevant details are complete, say so briefly and proceed rather than manufacturing gaps.

Then produce the requested design, procedure, or automation using known details and clearly marked assumptions. Keep unresolved details beside affected steps. An abstract scenario can remain a useful design, but it does not supply missing instructions for performing or observing the test. For case-only work, keep automation needs brief and do not generate unrequested code or require a tool choice.

## Apply the capabilities needed for the request

- For cases, validation workflows, or review of existing behavioral coverage, read [test-design.md](references/test-design.md).
- For evidence needs, interface/data/observation gaps, or executable binding inspection, read [discovery.md](references/discovery.md).
- For Gherkin or automation, read [rendering.md](references/rendering.md). Use design or discovery guidance when necessary for the requested output.
- Read [examples.md](references/examples.md) only when a concrete example helps a decision.

A direct case request need not produce a separate claim artifact. Rendering need not produce a separate MAP file. Discovery can inform either capability or answer a discovery-only request; do not run it universally. Reuse existing sources and bindings rather than restarting an inventory.

## Retain the behavioral contract

For each test, make the subject, relevant conditions, one challengeable commitment, expected observation, and contrary observation recoverable. Preserve material source values, units, exceptions, permissions, and boundaries. Label inferred and proposed behavior beside the affected test with its basis; do not quietly turn hypotheses into obligations.

Choose observation points that distinguish the asserted result from setup success or a related event. Use the smallest verification boundary sufficient to challenge the behavior. One assertion may need several tests; one scenario may address several assertions only when observations are attributable separately. IDs alone do not establish coverage.

When implementations or observations conflict with the source, retain the conflict. Discovering current behavior does not redefine expected behavior. Keep material interpretations separate, offer useful conditional designs, and ask only when the requested outcome cannot be meaningfully produced without a decision.

## Report what is actually delivered

Use these distinctions where material, without requiring a sequential workflow:

- **Designed:** conditions, actions, expected observations, and failure interpretation are specified; unknowns remain visible.
- **Rendered:** scenario syntax and meaning are checked; missing step bindings remain identified.
- **Bound:** required steps, interfaces, fixtures, and configuration are supported for the stated target; remaining limitations are disclosed.
- **Executed:** an actual run or supplied execution record identifies target/version, conditions, observations, and scoped result.

A feature file is not automatically runnable. Bound steps are not evidence of a pass. Parser or dry-run success is not behavioral execution. Distinguish contradiction from missing access, missing bindings, unusable observations, or environmental failure; those may make evaluation inconclusive.

For runnable automation, inspect available contracts and bindings and implement only supported details within authorized scope. Unknown selectors, endpoints, credentials, thresholds, or correlation rules must not be invented. Provide a useful draft and precise missing bindings when runnable completion is unsupported.

## Deliver and preserve useful links

Use the requested format. Default to readable Markdown for cases/findings and recommend reusable, business-readable Gherkin for rendered scenarios. For automation, ask for the user's preferred programming language and automation tool unless already supplied; if unanswered, retain Python/Behave as the default and state that assumption. Straightforward shell/PowerShell checks can proceed without that prompt. Apply the selection and reuse guidance in [rendering.md](references/rendering.md). Answer in chat when appropriate; save files when requested or needed. Keep optional detail proportional to the task.

Preserve source IDs and locators. In saved or repeated work retain assertion/test links, material bases, assumptions, discovery sources, relevant target/version, and actual result references when available. State reviewed scope and exclusions before claiming coverage. Revisions identify affected tests and conclusions without silently rewriting accepted baselines.

Routine discovery inspects only what the task needs. Behavior-changing probes belong to authorized execution, with bounded runs and necessary cleanup. Do not treat a request to design tests as authorization to exercise a live system. Development checks and evaluation files are maintenance tools, not runtime prerequisites.
