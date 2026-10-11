# RMC2 Reimbursement Monitoring Prototype

The selected main application is the original Prototype A. The main HTML, JavaScript, stylesheet, and logo exactly match the preserved dist/version-a files.

[Main prototype](https://rmc2-reimbursement-prototype.ironcloud1723.chatgpt.site/) · [Comparison page](https://rmc2-reimbursement-prototype.ironcloud1723.chatgpt.site/compare.html)

## Open locally

Open dist/index.html in a browser. No installation or build is required. Alternatively, run `python -m http.server 8765 --directory dist` and open http://localhost:8765.

## Editing

Use dist/app.js, dist/style.css, and dist/index.html as the source for small requested UI changes. Keep Prototype A's existing screens, navigation, dashboard, and interactions. The workflow, easy, and a-layout files are inactive retained implementations and are not loaded by the main homepage.

Versions A and B in their respective folders remain preserved comparison snapshots. The requirements and field mapping from supplied references remain documented in Workflow-Source-Mapping.md for future targeted implementation into Prototype A.

All records, files, messages, accounts, and connections are simulated. No real emails are sent. Session changes reset on reload and do not sync across devices. The hosted Site is private to its owner; GitHub pushes do not automatically update that deployment.
