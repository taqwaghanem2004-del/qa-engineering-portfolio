# Project Presentation: Advanced Playwright Project

Repository: https://github.com/taqwaghanem2004-del/playwright-advanced-qa

## Project overview
A Playwright and TypeScript test project that shows how to design a maintainable automation framework. It tests a public demo shop (SauceDemo) through the UI and a public demo API (Fake Store API).

## Testing scope
- UI: login, product sorting, cart and end-to-end checkout on SauceDemo
- API: three tests against the Fake Store API
- Mocked UI: a small local page that loads products from the API, tested with a success case and a 500 error case
- A deliberately flaky test and its fixed version

## Tools
Playwright, TypeScript, Page Object Model, fixtures, a test data factory, GitHub Actions, Git and GitHub.

## Testing activities
- Built page objects so locators live in one place and assertions stay in the tests
- Added a login fixture so every test gets its own browser context and tests can run in parallel
- Generated checkout data for each run instead of hard-coding it
- Used only Playwright auto-waiting and web-first assertions, with no fixed waits
- Mocked API responses with `page.route` to test success and error handling
- Investigated a flaky test with the HTML report and the Trace Viewer
- Set up a GitHub Actions workflow that runs the tests on every push

## Challenges and results
- Last full run: 14 tests, 14 passed, 0 failed (7.8 s).
- Flaky test: it read the page text once without waiting. In 20 runs it failed 9 times and passed 11 times. The Trace Viewer showed the page still displaying "Loading..." at the failing step. The fixed version, which waits for the expected text, passed 20 of 20 runs.
- CI: in the first GitHub Actions run, the Fake Store API returned HTTP 403 to the GitHub runners, so the 3 API tests failed there. The cause was not confirmed. The API tests are now skipped when running in CI, and the reason is documented. The UI tests, including the mocked ones, run in CI, and later runs passed.

## What I would improve
- Run the API tests in CI against a mocked or self-hosted API
- Add more browsers (only Chromium was used)