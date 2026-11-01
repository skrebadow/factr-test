# FACTR Test

Version 0.1.0. Design falsifiable tests, discover relevant evidence and bindings, and render scenarios or supported automation from available engineering context.

One [entry skill](skills/factr-test/SKILL.md) combines MAP, conditional discovery, and RENDER capabilities. Enter directly at the requested outcome. Test has its own inputs and workflow; it has no Agile handoff or integrated pipeline.

Test begins design, procedure, and automation work by identifying what is missing for an actionable test procedure and what automation would additionally need. It separates behavioral decisions from setup, data, action, observation, and cleanup details, then identifies missing bindings, fixtures, dependencies, and configuration. Each material gap includes its effect and how to resolve it. Supported work continues with visible unknowns; complete inputs lead directly to the requested output.

## Example requests

- “Design tests from this description; keep assumptions visible.”
- “Start with what is missing to write a repeatable test procedure and what we would need to automate it.”
- “Identify what evidence would distinguish rejection from successful processing.”
- “Inspect these contracts and step definitions to resolve the bindings this test needs.”
- “Render this behavior as Gherkin and identify unbound steps.”
- “Assess which failures these existing tests can detect.”

Core's methodology is bundled by version with [provenance](core-provenance.json). A separate Core installation, approved FACT Set, discovery sidecar, or HARDEN artifact is unnecessary.

Discovery distinguishes plans, source-backed findings, inferences, and actual observations. Test output distinguishes design, rendering, supported bindings, and actual execution. Draft Gherkin is not automatically runnable; a dry run or passing parser is not evidence of product behavior.

For automation, Test asks for your preferred programming language and automation tool when those choices are missing. If unanswered, it proceeds with Python/Behave and states that assumption. Straightforward shell or PowerShell checks can proceed without that prompt. Test recommends reusable, business-readable Gherkin with shared step bindings while honoring your chosen tool and output format. Case-only and Gherkin-only requests need no automation-stack choice.

## Optional output schemas

[Zephyr Manual Test](output-schemas/zephyr-manual-test.md) presents manual cases with a title and requirement ID, a Step / Test Data / Expected Result Markdown table using Given/When/Then, and unresolved execution details below it. It is a standalone output schema, separate from skill instructions. To select it, attach or reference the schema in your request: “Use FACTR Test to write a manual test scenario for this requirement, following output-schemas/zephyr-manual-test.md.” This produces Markdown; Zephyr import or publication requires its own target-specific format and authorization.

## Local registration

Register this repository's marketplace from its root:
~~~powershell
codex plugin marketplace add .
~~~

Install and enable FACTR Test through the host's plugin browser, then start a new chat or CLI session. Invoke `$factr-test` or select the plugin/skill with `@` where supported. Creating the package does not register, install, or enable it.

See the [official OpenAI plugin documentation](https://developers.openai.com/codex/plugins) for host behavior. Host installation has to be verified separately.

## Development

The local `evaluation/`, `scripts/`, and `tests/` directories are excluded from Git. When present, Python 3 supports the maintenance checks:
~~~powershell
python scripts/check_package.py --core-source ../factr-core
python -m unittest discover -s tests -v
~~~

The skill-creator validator can additionally check `skills/factr-test`; its own PyYAML dependency is a development dependency. The plugin itself has no Python runtime or build requirement. Generated Python automation may have dependencies specific to its target.

Local evaluation cases contain realistic requests and review criteria. Structural checks do not establish live reasoning quality, execution results, or performance improvement.

The icon retains FACTR Core's design in dark purple, gray, and light purple. Developer: Rebadow, Shauna-Kay (US) - MN.
