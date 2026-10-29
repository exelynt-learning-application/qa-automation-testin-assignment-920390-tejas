# SauceDemo Bug Reports

**Application:** [SauceDemo](https://www.saucedemo.com/)  
**Test type:** Exploratory manual testing  
**Scope:** Product details, cart, checkout, and usability

> **Evidence integrity note:** These are candidate bug reports based on publicly documented SauceDemo test scenarios. They have not been independently reproduced as part of generating this file. Before submitting, test each scenario on the current website, replace the Actual Result with what you personally observe, and attach your own screenshot. If a scenario cannot be reproduced, mark it **Not Reproduced** and replace it with a confirmed defect.

## Test environment

- Browser: Record the browser and version you actually use.
- Operating system: Record your actual operating system.
- Test date: Record the date you perform the test.
- Demo credentials: Use the public credentials shown on the SauceDemo login page. Candidate accounts below commonly use password `secret_sauce`.

## Bug summary

| Bug ID | Title | Test account | Severity | Priority |
|---|---|---|---|---|
| SD-BUG-001 | Product detail page displays an incorrect product image | `problem_user` | High | High |
| SD-BUG-002 | Add to Cart button does not respond on the product detail page | `problem_user` | High | High |
| SD-BUG-003 | Last Name field is not interactive during checkout | `problem_user` | High | High |
| SD-BUG-004 | Checkout button is positioned incorrectly on the Cart page | `visual_user` | Low | Medium |
| SD-BUG-005 | Finish button does not complete the order | `error_user` | Critical | High |

## Detailed reports

### SD-BUG-001 — Product detail page displays an incorrect product image

- **Test account:** `problem_user`
- **Severity:** High
- **Priority:** High
- **Precondition:** The user is logged in and has reached the page described in the steps.
- **Steps to reproduce:**
  1. Open https://www.saucedemo.com/.
  2. Sign in as problem_user using the public demo password secret_sauce.
  3. Select Sauce Labs Backpack from the Products page.
  4. Compare the product name and image on the detail page with the listing.
- **Expected result:** The detail page displays the correct image for the selected product.
- **Actual result:** Candidate issue based on public reports. Reproduce on the current site and replace this text with the exact observed result before submission.
- **Impact:** The mismatch may confuse customers about the product they are viewing.
- **Screenshot:** `screenshots/SD-BUG-001.png` — replace the placeholder image with your own browser screenshot after reproducing the issue.

### SD-BUG-002 — Add to Cart button does not respond on the product detail page

- **Test account:** `problem_user`
- **Severity:** High
- **Priority:** High
- **Precondition:** The user is logged in and has reached the page described in the steps.
- **Steps to reproduce:**
  1. Open https://www.saucedemo.com/.
  2. Sign in as problem_user using the public demo password secret_sauce.
  3. Open a product detail page.
  4. Click Add to Cart and inspect the button and cart badge.
- **Expected result:** The product is added to the cart, the button changes to Remove, and the cart badge increments.
- **Actual result:** Candidate issue based on public reports. Reproduce on the current site and record the exact result.
- **Impact:** The user may be unable to add the product to the cart from its detail page.
- **Screenshot:** `screenshots/SD-BUG-002.png` — replace the placeholder image with your own browser screenshot after reproducing the issue.

### SD-BUG-003 — Last Name field is not interactive during checkout

- **Test account:** `problem_user`
- **Severity:** High
- **Priority:** High
- **Precondition:** The user is logged in and has reached the page described in the steps.
- **Steps to reproduce:**
  1. Sign in as problem_user using the public demo password secret_sauce.
  2. Add a product to the cart and open the cart.
  3. Click Checkout.
  4. Try entering a value in the Last Name field on Your Information.
- **Expected result:** The Last Name field accepts text and the form validates required information clearly.
- **Actual result:** Candidate issue based on public reports. Reproduce and record what happens in the current session.
- **Impact:** Checkout may be blocked if the field cannot accept input.
- **Screenshot:** `screenshots/SD-BUG-003.png` — replace the placeholder image with your own browser screenshot after reproducing the issue.

### SD-BUG-004 — Checkout button is positioned incorrectly on the Cart page

- **Test account:** `visual_user`
- **Severity:** Low
- **Priority:** Medium
- **Precondition:** The user is logged in and has reached the page described in the steps.
- **Steps to reproduce:**
  1. Sign in as visual_user using the public demo password secret_sauce.
  2. Add a product to the cart.
  3. Open the Cart page.
  4. Inspect the Checkout button position relative to other controls.
- **Expected result:** The Checkout button appears in the intended action area with consistent alignment.
- **Actual result:** Candidate issue based on public reports. Reproduce and describe the exact layout seen.
- **Impact:** The layout may look inconsistent or make the next action less obvious.
- **Screenshot:** `screenshots/SD-BUG-004.png` — replace the placeholder image with your own browser screenshot after reproducing the issue.

### SD-BUG-005 — Finish button does not complete the order

- **Test account:** `error_user`
- **Severity:** Critical
- **Priority:** High
- **Precondition:** The user is logged in and has reached the page described in the steps.
- **Steps to reproduce:**
  1. Sign in as error_user using the public demo password secret_sauce.
  2. Add a product to the cart and open the cart.
  3. Click Checkout and complete the information form.
  4. On Checkout: Overview, click Finish.
  5. Observe whether the order confirmation page appears.
- **Expected result:** The order completes and the user sees an order confirmation page.
- **Actual result:** Candidate issue based on public reports. Reproduce on the current site and replace this text with the exact observed result.
- **Impact:** The user may be unable to complete the main purchase workflow.
- **Screenshot:** `screenshots/SD-BUG-005.png` — replace the placeholder image with your own browser screenshot after reproducing the issue.

## Bug life cycle

```text
New / Reported → Triaged → Assigned → In Progress → Fixed / Resolved
                                                   ↓
Closed ← Verified ← Retest ←───────────────────────┘

If retest fails: Retest → Reopened → Assigned / In Progress
Other possible states: Rejected / Invalid, Deferred / On Hold, Cannot Reproduce
```

### State descriptions

1. **New / Reported:** The tester logs the issue with title, environment, steps, expected result, actual result, and evidence.
2. **Triaged:** The team checks validity, reproducibility, scope, severity, and priority.
3. **Assigned:** The issue is assigned to a responsible developer or team.
4. **In Progress:** The developer investigates and works on a fix.
5. **Fixed / Resolved:** A code change is ready for QA verification.
6. **Retest:** The tester repeats the original steps on the fixed build.
7. **Verified:** The tester confirms the original issue no longer occurs.
8. **Closed:** The defect is formally closed after successful verification.
9. **Reopened:** The issue still occurs or the fix is incomplete, so it returns for further work.
10. **Rejected / Invalid:** The team determines it is not a defect, is a duplicate, or is expected behavior. Record the reason.
11. **Deferred / On Hold:** The defect is accepted but postponed due to release priorities or dependencies.
12. **Cannot Reproduce:** The team cannot reproduce the issue with the available details and requests additional evidence.

## Severity vs. priority

- **Severity** is how much the defect affects functionality or users.
- **Priority** is how urgently the team should fix it, considering business urgency, release timing, and user impact.

### Example 1: High severity, high priority
Checkout cannot complete because the Finish button does not work. This blocks the main purchase flow, so severity may be Critical/High and priority High/Urgent.

### Example 2: Low severity, high priority
A logo is slightly misaligned on the homepage just before a major product launch. Core functionality still works, so severity may be Low, but the business may prioritize the fix because the issue is highly visible.

## Before submitting

- [ ] Reproduce each issue on the current site.
- [ ] Update Actual Result with your own observation.
- [ ] Replace every placeholder with an original screenshot.
- [ ] If a scenario cannot be reproduced, replace it with a confirmed issue.
- [ ] Reassess severity and priority based on the observed impact.
- [ ] Verify that screenshots match their bug IDs.

## References

- [SauceDemo public demo](https://www.saucedemo.com/)
- [Public SauceDemo bug-report examples](https://github.com/sabari-priya-j/saucedemo-bug-reports)
- [SauceDemo testing portfolio](https://github.com/agbooluchi76-prog/SauceDemo-Testing-Portfolio-01)
- [SauceDemo testing portfolio and notes](https://github.com/ezethufokazi/SauceDemo-Testing)

Public references help identify scenarios to investigate; they do not replace your own reproduction and screenshots.
