# Bug Report Template

| Field | Value |
| :--- | :--- |
| **Bug ID** | `BUG-<PROJECT>-<NNN>` |
| **Title** | `<What breaks>` when `<action>` on `<screen>` |
| **Reported by** | |
| **Date reported** | |
| **Module / Feature** | |
| **Severity** | Critical / High / Medium / Low |
| **Priority** | P1 / P2 / P3 / P4 |
| **Status** | New / Open / In Progress / Fixed / Retest / Verified / Closed / Reopened / Deferred / Rejected |
| **Assigned to** | |
| **Build / Version** | |
| **Environment** | QA / Staging / Production |
| **Platform** | Browser + version, or device + OS version |
| **Reproducibility** | Always / Intermittent (x of y attempts) / Once |

---

### Preconditions

State the system must be in before step 1, including the account and data used.

### Steps to reproduce

1.
2.
3.

### Expected result

What the requirement says should happen.

### Actual result

What actually happened, quoting the exact error text or status code.

### Evidence

Screenshot, screen recording, console output, network trace, request/response body, or relevant log lines.

### Impact

Who is affected, how often, and whether a workaround exists.

### Additional notes

Regression? Related bug IDs? First build where it appears?

---

## Severity guide

| Severity | Meaning |
| :--- | :--- |
| **Critical** | System down, data loss or corruption, security breach, no workaround |
| **High** | Core function unusable, workaround is impractical |
| **Medium** | Function impaired, an acceptable workaround exists |
| **Low** | Cosmetic, wording, or minor UI issue with no functional impact |

## Priority guide

| Priority | Meaning |
| :--- | :--- |
| **P1** | Blocks the release — fix immediately |
| **P2** | Must be fixed before this release ships |
| **P3** | Fix in this release if capacity allows |
| **P4** | Backlog |

## Writing rules

- The title states the symptom, not the suspected cause.
- Steps start from a known state; no step assumes context the reader does not have.
- One defect per report.
- Severity is technical impact, set by QA. Priority is business urgency, set by the product owner.
- Attach evidence before submitting, not after being asked.
