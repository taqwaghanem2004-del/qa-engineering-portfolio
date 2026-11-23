# Manual Testing

## Overview
Manual testing of SauceDemo (https://www.saucedemo.com), a public demo e-commerce site. The work covers test scenarios, test cases with execution results, and bug reports.

## Scope
- 4 test scenarios: login, product browsing and sorting, cart management, checkout
- 18 test cases (positive and negative), all executed manually
- 4 bug reports, found with the demo user `problem_user`
- The site has no search box, so the Sort dropdown was used as the closest equivalent

## Results
- 16 test cases passed, 2 failed (TC-012 and TC-018), both linked to documented bugs
- Bugs found: 1 Critical, 1 High, 2 Medium

| Bug | Severity | Title |
|---|---|---|
| BUG-001 | Medium | Identical product images displayed for all products |
| BUG-002 | Medium | Sort/Filter dropdown does not apply the selected option |
| BUG-003 | High | "Remove" button does not remove the product from the cart |
| BUG-004 | Critical | Last Name field malfunction blocks the checkout process |

## Other manual testing work
- A fundamentals assignment on an e-commerce scenario: 10 test scenarios classified as smoke, regression and exploratory testing, detailed test cases, requirement analysis and a bug life cycle example.

## Files
- `Practical_QA_Assignment.docx`: scenarios, test cases, bug reports, and the automated tests that followed (see the Automation folder)

## Notes
- Only public demo credentials were used. No real data.