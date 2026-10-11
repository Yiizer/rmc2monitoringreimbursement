# RMC2 Reimbursement Monitoring Prototype

The selected main application uses Prototype A, with a focused requirements-checklist improvement. Its existing dashboard, navigation, branding, and other screens remain in place.

[Main prototype](https://rmc2-reimbursement-prototype.ironcloud1723.chatgpt.site/) · [Comparison page](https://rmc2-reimbursement-prototype.ironcloud1723.chatgpt.site/compare.html)

## Open locally

Open dist/index.html in a browser. No installation or build is required. Alternatively, run `python -m http.server 8765 --directory dist` and open http://localhost:8765.

## Editing

Use dist/app.js, dist/style.css, and dist/index.html as the source for small requested UI changes. Keep Prototype A's existing screens, navigation, dashboard, and interactions. The workflow, easy, and a-layout files are inactive retained implementations and are not loaded by the main homepage.

Versions A and B in their respective folders remain preserved comparison snapshots. The requirements and field mapping from supplied references remain documented in Workflow-Source-Mapping.md for future targeted implementation into Prototype A.

All records, files, messages, accounts, and connections are simulated. No real emails are sent. Session changes reset on reload and do not sync across devices. The hosted Site is private to its owner; GitHub pushes do not automatically update that deployment.

## Requirements checklist

Open a reimbursement's Requirements tab (the separate Documents tab has been removed). View a requirement's files and tick its checkbox when checked. Multiple receipts appear under one requirement. The checklist shows checked, unchecked, missing, and replacement states, with a checked count and one Prepare email action.

Initial email preparation requires every displayed requirement to be checked. Missing-file requests use the sample client's email, and newly prepared submissions include the checked files. Required attachments cannot be omitted accidentally when sending. The Casey sample demonstrates a missing incident letter and a file needing replacement; sample buttons let you complete that flow. A new Form simulation starts with all requirements unchecked.

Validated with browser interaction tests for the checklist, previews, missing files/replacements, email attachment gates, new submissions, original navigation, and desktop/tablet/phone layouts. These are fictional example requirements and files; live eligibility rules and Google integrations are not implemented.
