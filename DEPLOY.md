# Publish the demo: quick guide

The `index.html` file is the complete, standalone app. No API, build step, runtime, backend or database is required. The demo should be published **only after** the applicant reviews its legal and functional accuracy.

## Option A — Netlify Drop (easiest, no code)
1. Open https://app.netlify.com/drop and sign in or create an account.
2. Extract `Prighter_Legal_Engineering_Portfolio.zip` into a folder.
3. Drag the **folder containing `index.html`** into the Netlify Drop page (or upload it as supported by the UI).
4. Netlify provides a `*.netlify.app` address. Open the address and verify all four demo scenarios and exports.
5. Optionally rename the site in Netlify to a professional label (subject to availability).
6. Put the **actual, verified URL** in the application email. Do not claim that a demo is live until it is actually accessible.

## Option B — GitHub Pages (source is reviewable)
1. Sign into GitHub and create a repository, e.g. `eu-representative-compliance-navigator`.
2. Upload the project files at repository root, ensuring `index.html` is at the root (or use the GitHub app connection in ChatGPT after connecting it).
3. Repository **Settings > Pages**: deploy from branch `main`, root `/` (exact labels can vary).
4. Once published, GitHub provides an HTTPS Pages URL. Open it to test manually.
5. A public repository makes the code and README public. If you prefer not to publish code publicly, choose another hosting method and check account settings.

## Post-deploy checks
- [ ] Open on a phone and desktop browser.
- [ ] Select each of the four fictional demo scenarios; outcomes update live.
- [ ] Modify a single answer; only the relevant rules change.
- [ ] Download the JSON assessment and test Print / Save as PDF.
- [ ] Check EUR-Lex links.
- [ ] Verify that the site loads without external libraries or analytics.
- [ ] Confirm the legal disclaimer and project authorship description.

## Privacy and compliance
No data is sent to a server by the app. A **hosting provider** may separately log requests to serve the page under its own policies. For public demos, avoid entering real personal or client information. The site is a non-binding preliminary screening demonstration, **not legal advice**. No confidential material is incorporated.