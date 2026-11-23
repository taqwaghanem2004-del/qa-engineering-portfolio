# AI in Software Testing

Full assignment with evidence, reports and prompt log:
https://github.com/taqwaghanem2004-del/ai-qa-assignment

Test site: https://www.saucedemo.com (public demo credentials). AI tool used: Claude.
Every AI output was reviewed by a human, and the AI-generated and manually reviewed parts are documented.

## What was done
- Test case generation: 25 AI test cases reviewed on the real site (17 accepted, 5 modified, 3 rejected)
- Requirements analysis with AI
- AI-generated Playwright script, with code review and locator checks
- Self-healing test automation: explanation and a demo with a deliberately changed locator
- Visual regression testing with Playwright screenshot comparison
- Log analysis with AI (41-line sample log)
- Defect prediction from a sample defect history (34 defects), reported as predictions only
- AI-assisted QA workflow (7 stages with human review)
- Validation of AI output: 14 issues found and documented

## Deviations
- The practice site has no search box, so product sorting was automated instead.
- Applitools sign-up was not accepted, so Playwright's built-in screenshot comparison was used.
- Only Chromium was used.