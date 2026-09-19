# QA Test Documentation Templates

Reusable, release-ready QA documentation templates I use on Agile/Scrum projects — the artifacts that sit between a requirement and a signed-off release.

Automation gets the attention, but most of the quality work on a product is documentation: a test plan the team agrees on, test cases someone else can run, bug reports a developer can reproduce on the first read, and a traceability matrix that proves nothing was missed. These are the formats I have refined across fintech and HRM releases.

## Contents

| File | Purpose | When it is written |
| :--- | :--- | :--- |
| [`TEST-PLAN-TEMPLATE.md`](TEST-PLAN-TEMPLATE.md) | Scope, approach, environments, entry/exit criteria, risks | Start of a release cycle |
| [`TEST-CASE-TEMPLATE.md`](TEST-CASE-TEMPLATE.md) | Structured functional / regression / integration test cases | After requirements are frozen |
| [`BUG-REPORT-TEMPLATE.md`](BUG-REPORT-TEMPLATE.md) | Defect report with severity, priority, and reproduction steps | During execution |
| [`REQUIREMENT-TRACEABILITY-MATRIX.md`](REQUIREMENT-TRACEABILITY-MATRIX.md) | Requirement → test case → defect mapping | Throughout, reviewed at exit |
| [`EXAMPLE-bug-report.md`](EXAMPLE-bug-report.md) | A worked example of the bug report format | Reference |

## How I use them

1. **Plan** — fill the test plan, agree scope and exit criteria with the product owner and dev lead.
2. **Design** — write test cases against each acceptance criterion and log them in the RTM.
3. **Execute** — run the suite, record pass/fail, raise defects using the bug report format.
4. **Verify** — retest fixed defects, run the regression pass, update the RTM.
5. **Sign off** — confirm every exit criterion is met, or state explicitly which are not and why.

## Conventions

- **Severity** describes technical impact; **priority** describes business urgency. They are set by different people and they are not the same field.
- Every test case has exactly one expected result.
- Every bug report must be reproducible from the report alone, with no verbal follow-up.
- A defect is closed by the reporter, never by the fixer.

## License

MIT — use them, adapt them, no attribution needed.
