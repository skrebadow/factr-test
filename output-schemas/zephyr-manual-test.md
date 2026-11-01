# Zephyr Manual Test output schema

An optional presentation format for FACTR Test manual scenarios. Apply it when requested; it does not change the skill's default output. This schema describes Markdown output, not a Zephyr import file or integration.

## Formatting contract

Present each test case as a Markdown table with exactly three columns: **Step**, **Test Data**, and **Expected Result**. Use Given/When/Then wording, one clear setup or action per row, concrete test data, and observable expected results. Use “—” where no data or expected result applies. Put the test title and requirement ID above the table, and briefly identify any unresolved execution details below it.

- Use Given rows for setup, When rows for actions, and Then rows for observation or verification. Split compound steps into separate rows; do not assume the expected product outcome in setup.
- Put concrete values, units, roles, and fixture references in Test Data when supported by the source. Label illustrative values and assumptions; do not invent accepted inputs, selectors, commands, deadlines, or requirement IDs.
- Describe observable outcomes in Expected Result, including supported boundaries and rejection behavior. A setup or action row may also have an observable expected result when applicable.
- Use “—” only for an inapplicable cell. Mark an unknown but necessary value or method as unresolved in its affected row, then explain the missing detail and how to resolve it below the table.
- Preserve supplied requirement IDs and links above the table. Use a separate title and table for each test case. When no execution details remain unresolved, state “Unresolved execution details: None identified in the supplied context.” This describes procedure completeness, not execution or a passing result.

## Layout

Replace the placeholders with supported case details. Add or remove rows to fit the actual procedure; the example row count is not a requirement.

~~~markdown
**Test title:** <Descriptive test title>
**Requirement ID:** <Supplied requirement ID and source link, or Unresolved>

| Step | Test Data | Expected Result |
| --- | --- | --- |
| Given <one setup instruction> | <Concrete setup data or —> | <Observable setup result or —> |
| When <one action instruction> | <Concrete action data or —> | <Observable action result or —> |
| Then <one observation or verification instruction> | <Concrete comparison data or —> | <Observable required outcome> |

**Unresolved execution details:** <Affected step, missing detail, and information or inspection needed to resolve it; or None identified in the supplied context.>
~~~
