# Conditional discovery

Discovery resolves information needed for test conditions, stimuli, observations, or executable bindings. It can inform design or rendering and can be requested on its own. It is not a mandatory MAP-to-RENDER transition.

## Assess what a procedure and automation need

Begin with the supplied behavior and requested test boundary. Distinguish these needs where relevant:

- **Behavioral decisions:** expected outcome, concrete constraints, exceptions, and the contrary observation. Missing requirements need clarification or labeled conditional designs; implementation discovery does not decide them.
- **Procedure details:** target/version, actor and access, initial state, valid or deliberately invalid test data, how to establish setup and perform the stimulus, where and how to observe the outcome, correlation and any supported timing bound, evidence to retain, and reset/cleanup.
- **Automation requirements:** machine-accessible actions and observations, supported contracts or selectors, reusable step definitions, fixtures and data builders, language/tool choice, installed dependencies and runner configuration, credential references, and bounded polling or cleanup where needed.

These are considerations for the actual test, not a questionnaire to ask in full. An established item is not a gap; an irrelevant item need not be reported. A manual procedure may be complete while automation still lacks a machine-readable observation or binding.

Lead the result with unresolved needs, their effect on the procedure or automation, and concrete resolving actions or sources. Distinguish details that prevent a meaningful expected result from details that prevent a repeatable procedure or runnable automation. Resolve supported facts through nearby inspection when available; ask the user for material decisions or unavailable information. Retain provisional steps and precise unknowns when completion is unsupported. Follow [rendering.md](rendering.md) for language/tool preferences, the unanswered-question fallback, and the simple-shell exception when automation selection matters.

## Plans and findings are different

**Discovery guidance** identifies a gap, why it matters, plausible sources, and what finding would resolve it. Proposed commands, fixtures, logs, selectors, or interfaces remain suggestions.

**Actual discovery** inspects relevant supplied or accessible material and records findings with a supporting locator or observation. Distinguish:
- Source-backed contract/configuration/code details.
- Bounded inference with its premises.
- Suggested probe or candidate surface.
- Unresolved gap.
- Actual runtime observation with relevant target/version and conditions.

Code or documentation can establish a supported binding without demonstrating runtime success. Runtime observations cannot create missing obligations. A plausible implementation detail is not established merely because it makes the test concrete.

## Keep scope bounded

Start with the uncertainty that changes the requested result. Inspect the nearest useful source and reuse existing findings. Expand only when a remaining material gap warrants it. Do not inventory the whole environment, recursively inspect unrelated projects, or search for every possible observation surface.

Useful targets include:
- Actor/access model and intended system target.
- Interface contract, input schema, policy baseline, and valid/invalid data constraints.
- Observable outcome, correlation key, and established observation window.
- Existing step definitions, fixtures, libraries, object maps, and configuration.
- Runtime state relevant to the proposed test, when inspection is authorized.

Technology-neutral candidates can include an interface result, processing disposition, controlled record, report, diagnostic output, measurement, or device observation. Give a concrete inspection command only when its interface and parameters are supported; otherwise identify the needed contract instead of inventing a route.

## Make findings usable

For saved findings retain as much as the task needs:
- Gap or discovery question.
- Finding and support basis.
- Source reference/excerpt or actual observation record.
- Relevant target, revision, and conditions when available.
- Affected precondition, input, action, assertion, or binding.
- Remaining limitation, conflict, or resolving action.

A compact table or linked note is sufficient. No universal schema, approved sidecar, confidence score, or governed handoff is required. Close a gap only when its finding supports the actual target and needed detail.

A log mentioning a message is not necessarily evidence of its rejection. An available endpoint does not establish permission to use it, the applicable schema, or the resulting disposition. Keep those relationships explicit.

## Access and action boundaries

Routine discovery is inspection. Use supplied information first and only authorized access. Do not reveal secret values in records; refer to credential/configuration locations when useful.

A behavior-changing submission, restart, data mutation, or test run is execution rather than routine inspection. When requested and authorized, bound the target, actions, run count, observations, and necessary cleanup. Authorization to generate an automation file does not itself authorize executing it against a live environment.

If access or bindings are unavailable, report the precise unresolved issue and deliver the useful design or draft rendering that remains possible. Missing runtime access is not a reason to refuse all test design.
