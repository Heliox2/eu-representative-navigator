# EU Representative Compliance Navigator

**Independent portfolio exercise | Legal Engineering | Version 1.1 | 21 October 2026**

A fully client-side, rules-based web application demonstrating how EU legal obligations can be converted into auditable decision logic, user questionnaires and human-review escalations.

## Preview and run
Open `index.html` directly in a modern browser. No API keys, database, build tools, dependencies, login or internet access is needed. Select one of the four fictional demo scenarios to test the assessment engine.

## Why this project
Designed as an original application proof of concept for a Legal Engineer role. It demonstrates statutory scoping, rule design, uncertainty handling, legal content design, QA and documentation. It is **not** represented as prior professional client work. The interface and engineering implementation were developed with AI assistance; the applicant should validate the legal analysis, assumptions, design and tests before personally presenting it.

## Modules
- **GDPR**: Article 3(2) extraterritorial trigger and Article 27 representative obligation/exceptions.
- **DSA**: Article 13 designation for a non-EU provider of intermediary services offered in the Union.
- **EU AI Act**: Article 54 designation for non-EU GPAI-model providers, Article 54(6) open-source exception and Article 111(3) transitional timing. The separate high-risk AI system Article 22 pathway is out of scope.

The outcome vocabulary is explicit: `required`, `not_indicated`, `review`, `transition`. Unknown factual inputs lead to a `review` determination where a reliable conclusion cannot be established.

## Architecture
`Questionnaire (browser input) -> pure JavaScript decision engine -> reasoned legal outcomes -> HTML display / browser-based JSON and print-to-PDF export`

The application is single-file (`index.html`), including styling and the rule engine for offline portability. `decision-engine.js` is the standalone copy of the same pure rules for audit and unit tests; `test_engine.js` contains 16 regression cases.

**Test command:** `node test_engine.js` (Node.js needed only to rerun the tests, not to use the app).

## Files
- `index.html`: self-contained app, intended for hosting or review.
- `Product_Technical_Brief.pdf`: concise two-page product and technical design document.
- `decision-engine.js`: extracted rule engine for review/tests.
- `test_engine.js`: automated test harness.
- `TEST_CASES.md`: examples and known human-review boundaries.
- `DEPLOY.md`: static hosting and post-deployment steps.
- `netlify.toml`: optional security-related hosting headers for Netlify.
- `sample_assessment.json`: fictional, reproducible structured output.

## Limitations
This product screens selected representation pathways only, not full compliance, and does not make definitive classification decisions about targeting, establishment, system type, risk or licensing. Nothing is sent over the network by the code; there is no data persistence or real client data.

## Primary source texts
- GDPR: https://eur-lex.europa.eu/eli/reg/2016/679/oj/eng
- DSA: https://eur-lex.europa.eu/eli/reg/2022/2065/oj/eng
- AI Act: https://eur-lex.europa.eu/eli/reg/2024/1689/oj/eng
- European Commission GPAI guidance: https://digital-strategy.ec.europa.eu/en/policies/guidelines-gpai-providers

The legal reference date is **21 October 2026**. Check for new legislation and guidance before any real use.