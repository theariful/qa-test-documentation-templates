# Example — a bug report written to the template

A worked example showing the level of detail the template is meant to produce. Written against a public demo application so it can be reproduced by anyone.

---

| Field | Value |
| :--- | :--- |
| **Bug ID** | BUG-DEMO-014 |
| **Title** | Cart badge keeps a removed item's count after the product page is reopened |
| **Reported by** | Md Ariful Haque |
| **Date reported** | 2026-09-12 |
| **Module / Feature** | Shopping cart — item count badge |
| **Severity** | Medium |
| **Priority** | P2 |
| **Status** | New |
| **Build / Version** | 1.4.2-qa |
| **Environment** | QA |
| **Platform** | Chrome 128.0 / Windows 11 |
| **Reproducibility** | Always (5 of 5) |

### Preconditions

Logged in as a standard user with an empty cart.

### Steps to reproduce

1. Open the products listing page.
2. Click **Add to cart** on "Backpack". The cart badge shows `1`.
3. Click **Remove** on the same product. The badge clears.
4. Navigate to the product detail page for "Backpack".
5. Press the browser back button to return to the listing.

### Expected result

The cart badge stays empty, because the cart contains no items.

### Actual result

The cart badge shows `1` again. Opening the cart page shows it is empty, so the badge and the cart disagree. The badge value is read from a cached count rather than the live cart state.

### Evidence

- Screenshot: badge showing `1` alongside an empty cart page.
- `GET /api/cart` returns `{"items": [], "count": 0}` while the badge renders `1`.

### Impact

Every user who removes an item and then navigates back sees a wrong cart count. No data is lost and checkout is unaffected, but the count is not trustworthy and generates support contacts.

### Additional notes

Not reproducible in build 1.4.0-qa — appears to be a regression introduced with the client-side cart caching in 1.4.1.
