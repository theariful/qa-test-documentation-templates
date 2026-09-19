# Test Cases — `<Module>`

| Field | Value |
| :--- | :--- |
| Module | |
| Requirement ref | |
| Author | |
| Version | |
| Last updated | |

---

## Test case format

| Field | Description |
| :--- | :--- |
| Test Case ID | `TC-<MODULE>-<NNN>` |
| Title | Action and expected outcome in one line |
| Type | Functional / Regression / Integration / Negative / Boundary / API |
| Priority | High / Medium / Low |
| Preconditions | State the system must be in before step 1 |
| Test data | Exact values used |
| Steps | Numbered, one action each |
| Expected result | One observable, verifiable outcome |
| Actual result | Filled at execution |
| Status | Pass / Fail / Blocked / Not Run |
| Defect ID | If failed |

---

## Suite

| ID | Title | Type | Priority | Preconditions | Test data | Steps | Expected result | Status | Defect |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| TC-LOGIN-001 | Valid credentials log the user in | Functional | High | User account exists and is active | `user@example.com` / `Valid#123` | 1. Open login page<br>2. Enter email<br>3. Enter password<br>4. Click **Log in** | Dashboard loads and the user's name appears in the header | Not Run | |
| TC-LOGIN-002 | Invalid password is rejected | Negative | High | User account exists | `user@example.com` / `Wrong#123` | 1. Open login page<br>2. Enter email<br>3. Enter wrong password<br>4. Click **Log in** | Error "Invalid email or password" is shown; the user stays on the login page; no session is created | Not Run | |
| TC-LOGIN-003 | Password field enforces the maximum length | Boundary | Medium | Login page open | 65-character string | 1. Focus the password field<br>2. Paste a 65-character string | The field accepts at most 64 characters | Not Run | |
| TC-LOGIN-004 | Account locks after 5 failed attempts | Functional | High | User account exists and is unlocked | Wrong password × 5 | 1. Submit an incorrect password 5 times | After the 5th attempt the account is locked and a lockout message is shown | Not Run | |

---

## Execution summary

| Metric | Count |
| :--- | :--- |
| Total | |
| Passed | |
| Failed | |
| Blocked | |
| Not Run | |
| Pass rate | % |
