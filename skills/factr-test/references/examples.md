# Constructed examples

These are illustrative reasoning examples, not runtime findings or execution results.

## Direct design without system access

Input: Only administrators may set retention from 7 to 30 days inclusive; rejected updates leave the saved value unchanged.

Derive commitments for permitted updates, role rejection, out-of-range rejection, and unchanged saved state after rejection. Keep 7 and 30 inclusive and preserve the administrator role. Do not invent integer-only input syntax, response codes, audit logs, or a response deadline.

One rejected update may challenge rejection and unchanged-state commitments with separately attributable observations. Several boundary cases may challenge the same range rule. Without access, deliver the design and identify how rejection and saved state must be observed.

## Discovery for invalid messages

Input: The receiver rejects messages that violate the supplied schema. Only the schema and a description are available.

Specify a deliberately invalid illustrative fixture relative to the supplied schema. Discover or identify the receiver's supported submission interface, applicable schema baseline, observable rejection boundary, and correlation mechanism when needed. Do not substitute sender acceptance or a related log for receiver rejection. No interface route or runtime result is established from the description alone.

## Draft rendering without bindings

Input: Saved notification preferences appear when the same operator reopens settings.

Illustrative Gherkin:
~~~gherkin
Feature: Recall saved notification preferences

  Scenario: Reopening settings displays saved preferences
    # Expected behavior supplied in the description; steps are unbound.
    Given an operator has saved supported notification preferences
    When that operator reopens the settings page
    Then the displayed preferences match the saved preferences
~~~

This is a rendered design, not runnable automation or evidence of a pass. Binding discovery may identify existing save, reopen, and compare steps. Restart persistence, sign-out, and cross-device behavior remain unspecified.

## Conflicting evidence

A requirement expects rejected updates to preserve the saved value; an actual correlated observation shows that the value changed. Report contradiction within the observed target/conditions. Do not redefine rejection as permitted mutation to match implementation. If the record cannot identify the submitted update or saved value, report the observation gap rather than asserting contradiction.

## Discovery-only request

A user asks where a delivered message's effective priority can be observed. Inspect relevant documentation, supplied records, or supported runtime surfaces within access scope. Return supported findings and unresolved relationships. Do not create a workflow or feature file just to satisfy an assumed stage chain.
