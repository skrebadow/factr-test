# Rendering and supported automation — RENDER capability

Accept available requirements, assertions, cases, or workflows directly. Recommend reusable, business-readable Gherkin while honoring the user's requested format. No approved HARDEN workflow is required.

Lead with the procedure details and automation requirements still missing for the requested target, reusing the entry skill's assessment. Separate an unspecified action or observation method from a known method that lacks a step binding, fixture, dependency, or runner configuration. Use [discovery.md](discovery.md) when inspection can resolve a material gap, then render supported behavior with remaining gaps attached to the affected steps.

## Choose the automation target

Before generating language- or tool-specific automation, ask together: "What programming language do you prefer, and which automation tool or framework would you like to use? If you have no preference, I'll use Python with Behave and reusable Gherkin." Reuse choices already supplied in this conversation; ask only for a missing choice that matters. Inspect relevant project tooling to make a compatible recommendation, but do not treat its presence as the user's preference. If the user requests a recommendation or delegates the choice, propose a suitable combination and explain why.

Give the user a reasonable opportunity to answer. If the question goes unanswered, proceed with the existing Python/Behave default and label it as an assumption, rather than asking repeatedly or blocking completion. Preserve any partially supplied preference and choose a compatible fallback for the missing choice; do not replace a chosen language or tool to force Python/Behave. A fallback choice does not establish dependencies, supported bindings, or authorization to execute.

Skip the preference prompt when a straightforward shell or PowerShell script can handle the required setup, actions, observations, assertions, and cleanup using supported interfaces and available utilities. State the chosen shell and why it suffices. Honor any supplied language/tool preference. Small code size alone does not justify the exception when the behavior needs browser interaction, specialized fixtures, or a framework-specific runner.

Case-only, discovery-only, and Gherkin-only requests need no programming-language or runner decision. While awaiting a preference, continue with language-neutral scenarios and supported binding discovery; generate target-specific code once the user answers or the stated fallback applies.

Steer toward reusable Gherkin by explaining that scenarios can describe stable behavior while step definitions implement it in the chosen stack. Recommend a compatible Gherkin runner or integration when useful, preserving the user's tool choice. Do not require a new framework, feature file, or dependency for a simple script or when another format is requested; retain links between any scenarios and their script checks. Gherkin remains a rendered specification until its bindings and execution are verified.

## Preserve the behavioral meaning

Write a meaningful Feature and concise Scenario titles. Preserve supplied IDs as valid tags or comments when useful. Keep assertion/source links recoverable; use comments or an adjacent trace note rather than imposing exact source text above every scenario.

Given defines relevant context; When introduces the stimulus or observation action; Then asserts the observable commitment. Do not make an expected system result a prerequisite or a performed action. Preserve concrete permissions, data boundaries, exceptions, and failure meaning.

Use Background only for truly common context. Use Scenario Outline and Examples when meaningful data variation reduces duplication. Ensure each substituted value has a defined role and does not erase different expected outcomes.

Reuse step vocabulary and parameterized definitions for the same behavioral action or observation across scenarios. Keep selectors, transport details, and other implementation mechanics in bindings so scenarios remain reusable when those mechanics change. Do not merge steps whose preconditions, outcomes, or failure meanings differ merely because their wording is similar.

One assertion may have several scenarios. One scenario may cover several assertions only with separately attributable observations. Do not enforce one-to-one mappings or an immutable title that no longer describes scope.

## Reuse supported bindings

Inspect supplied step libraries and relevant automation context when actual bindings matter. Prefer compatible existing vocabulary and stable object/resource identifiers. Generic framework conventions are not evidence of this project's interfaces.

A rendered scenario may use business-readable unbound steps or explicit placeholders. Identify them outside the executable path or in concise comments. Do not invent selectors, endpoints, payload fields, output keys, or credentials to pretend they are bound.

For runnable automation, verify the required step definitions, fixtures, dependencies, target configuration, and supported interface mappings. Implement missing bindings only when their behavior and interfaces are sufficiently supported. A step that only raises an unimplemented error is a draft stub, not bound automation.

Match retries, polling, time limits, and cleanup to supported behavior and environment. Do not hide a failure with unbounded retries or introduce an invented timing requirement.

## Check the delivered status

- Check Gherkin syntax with an available parser when practical. If syntax was only inspected, say so.
- Check binding resolution through relevant library inspection or an available framework dry run. A dry run establishes parsing/binding readiness within its scope, not executed behavior.
- Report missing steps, fixture/configuration gaps, and unsupported interfaces accurately.
- Execute only when requested or otherwise authorized for the target and actions. Record actual observations, command/run context, result, and limitations.

An observation failure caused by absent permissions, correlation, fixture, or binding may be inconclusive. Distinguish it from contrary evidence of the product behavior. Passing checks support only the tested scope.

## Output

Deliver the requested feature file, supporting code when justified, and concise status. Keep source/behavior links and unresolved bindings durable in the file or accompanying note. Do not imply that syntactically valid Gherkin or compiled code has run.

For a case-only request, stop at the useful case; do not produce code by default. For a rendering-only request, produce the supported draft and exact gaps without demanding a separate test-design artifact. Discovery can be used wherever resolving a gap materially improves the requested output.
