# Automation Testing (Playwright)

Two Playwright projects, each in its own repository with a full README:

## 1. Advanced Playwright Project (TypeScript)
https://github.com/taqwaghanem2004-del/playwright-advanced-qa

- Page Object Model, fixtures, test data factory, parallel execution
- UI tests (SauceDemo) and API tests (Fake Store API), mocked UI tests
- Investigation of an intentionally flaky test (failed 9 of 20 runs; fixed version passed 20 of 20)
- Last full run: 14 tests passed
- CI note: the 3 API tests are skipped in GitHub Actions because the API returned HTTP 403; the cause was not confirmed

## 2. Playwright Training Project (JavaScript)
https://github.com/taqwaghanem2004-del/playwright-training

- UI checkout test with Page Object Model (SauceDemo)
- Reusable login fixture with saved session
- API tests (JSONPlaceholder)
- GitHub Actions CI pipeline with HTML report artifact
- Written QA analysis of a Dynamics 365 purchase order workflow (documented only, not executed)