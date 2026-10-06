# RMC2 Reimbursement Monitoring Prototype

Interactive reimbursement workflow prototype with fictional data. No Google account connections or real email sending are enabled.

## Try the published prototypes

[Compare Version A and Version B](https://rmc2-reimbursement-prototype.ironcloud1723.chatgpt.site/compare.html)

The published site currently requires access through its owner's account.

## Open locally

Download or clone this repository, then open `dist/compare.html` in a browser. Choose either prototype:

- **Version A** (`dist/version-a/index.html`): the previous dashboard design.
- **Version B** (`dist/version-b/index.html`): the simplified design with dates and guided document review.
- **Current working prototype** (`dist/index.html`): the current homepage, available for future development.

No package installation or build step is required. For a local web server, run `python -m http.server 8765 --directory dist`, then open http://localhost:8765/compare.html.

## Included workflows

Sample request submission, document review, attachment selection, email composition and simulated sending, incoming replies, requirement checks, follow-ups, status changes, history, and CSV reporting.

All data is fictional and held in the browser session. Reloading starts fresh; actions do not sync between devices. Demo identities do not provide authentication. Version B uses an illustrative October 6, 2026 clock.

## Files

- `dist/`: self-contained static HTML, CSS, JavaScript, and branding assets.
- `dist/version-a/` and `dist/version-b/`: preserved comparison snapshots. Keep these unchanged when editing the current prototype.
- `Prototype-Guide.md`: walkthrough and prototype limitations.
- `Prototype-Comparison.md`: comparison instructions.
- `prototype-snapshots.json`: source commit references from the original Sites repository; these are historical references, not commits in this GitHub repository.

The public-facing prototype remains hosted through Sites. Pushing this repository does not automatically publish or update that site.
