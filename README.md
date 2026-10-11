# RMC2 Reimbursement Monitoring Prototype

Interactive prototype with fictional records. No Google connections or real email sending are enabled.

## Open

[Latest workflow](https://rmc2-reimbursement-prototype.ironcloud1723.chatgpt.site/) · [Compare preserved designs](https://rmc2-reimbursement-prototype.ironcloud1723.chatgpt.site/compare.html)

The hosted site is private to its owner. To open locally, download or clone this repository and open dist/index.html in a browser. Open dist/compare.html for the preserved Version A and Version B designs. No package installation or build is required.

Alternatively, run `python -m http.server 8765 --directory dist` and open http://localhost:8765.

## Current flow

Review request and attachments → Prepare email → Replies and decision → Payment. Request navigation stays on the side; there is no separate Documents tab. Payment records the actual reimbursed amount, date, AMAPHIL/RMC2 processor, and email evidence separately from incurred and approved amounts.

## Source

- dist/index.html, workflow.js, workflow.css: current prototype.
- dist/version-a and dist/version-b: preserved comparison snapshots; leave unchanged.
- Other root scripts/styles are retained legacy assets and are not loaded by the current homepage.
- Prototype-Guide.md: walkthrough and limitations.
- Workflow-Source-Mapping.md: field mapping, conditional requirements, and reference context. No private records or source attachments are included.
- prototype-snapshots.json: historical commit references from the original Sites repository, not this GitHub history.

All data and drafts are held in the page session and reset on reload; nothing syncs across devices. Demo clock: 11 October 2026. Authentication, Google access, real email matching, and persistent storage remain future work.

The prototype remains hosted through Sites. A GitHub push does not automatically update that deployment.
