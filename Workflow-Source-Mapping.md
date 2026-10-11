# RMC2 workflow update — 11 October 2026

The current prototype is `dist/index.html`. Versions A and B remain unchanged under their existing folders. `dist/compare.html` links to all three. The new workflow uses `workflow.js` and `workflow.css`; the earlier root scripts are retained but are not loaded by the new homepage.

## Workflow

1. **Review request:** application details, applicability of requirements, all attached files, inline previews, review checks, and replacement handling. There is no separate Documents page or tab.
2. **Prepare email:** recipients, CC, template, subject, body, and attachment selection. Supports multiple addresses separated by commas or semicolons; keeps the request ID in the subject. Missing-requirement emails can be sent before the initial reimbursement submission.
3. **Replies & decision:** email evidence, follow-up reminders, and explicit approval/denial confirmation. Approval records an approved amount and does not mark the request paid.
4. **Payment:** payment email evidence, actual amount reimbursed, payment date, and processor (AMAPHIL or RMC2). Amount differences require an explanatory note. Payment does not overwrite incurred or approved amounts.

Activity and notes remain accessible from the request sidebar. All data and messages are fictional, held in memory, and reset on reload. Demo date: 11 October 2026, Asia/Manila. No Google connections or automatic extraction from real emails are implemented.

## Source field mapping

Reviewed the locally supplied Form Responses workbook, monitoring workbook, claim-form PDF, and email screenshot. Real applicants, diagnoses, bank details, Drive URLs, and source workbooks are not included in the prototype or repository.

| Form responses column | Source heading | Proposed application field |
|---|---|---|
| A | Timestamp | Request received |
| C | Customer Name | Client |
| E | Email Address | Applicant email (distinct from submitter address in B) |
| F | HMO Provider | Provider |
| G | Type of Availment | OPD / ER (Emergency) / ADMISSION |
| H | Date of Availment | Date of availment |
| I | Name of Facility (Hospital / Clinic) | Facility |
| M | Amount of Availment | Amount incurred |
| N | Reason for Reimbursement Request | Reason |
| V | STATUS | Legacy status requiring normalization |
| W | Process | Legacy processor; values include AMAPHIL, RMC2, and IWC |

The current prototype is the AMAPHIL workflow and uses AMAPHIL/RMC2 as requested. Other providers and historical IWC values must be preserved during a future import, not forcibly converted to either processor.

## Six attachment columns

| Column | Requirement category | Handling |
|---|---|---|
| L | Medical abstract | Admission; confirm applicability |
| O | Incident letter for reimbursement request | Separate from accident evidence |
| P | Laboratory / diagnostic request by physician | Laboratory/diagnostic procedures |
| Q | Sales invoice / official receipt with BIR TIN | May contain multiple receipt files |
| S | Itemized breakdown of charges | PDF specifies inpatient/confinement; review any uploaded copy |
| T | AMAPHIL reimbursement form | Completed claim form and signatures |

For the future connector: enumerate all Drive URLs in each cell, not only the first; include actual hyperlink targets when present; normalize Drive file IDs; deduplicate files within a request while preserving requirement associations. A filename without an accessible file ID is unresolved, not a successfully retrieved attachment. The local workbooks were inspected; the private linked Drive files were not downloaded or verified.

## Additional requirements from the supplied 2023 V2.1 PDF

- Original official receipts.
- Medical certificate with final diagnosis for inpatient and outpatient laboratory; the completed attending physician report is offered in lieu of a certificate.
- Medical abstract where applicable.
- Doctor's order for laboratory tests.
- Doctor's prescription for outpatient medicines.
- Itemized statement of account for inpatient/confinement.
- Police report for vehicular accident; affidavit for other incidents.
- Claim identity, membership, treatment, bank details, and signatures must be checked in the submitted form. The prototype does not collect real bank details.

The PDF states submission of the form and original documents to HR within 30 days of availment, standard payment processing of 15 working days after complete documents, and a minimum PHP25 bank charge. These are source-form notes, not independently verified current policies. The prototype does not deny requests automatically, promise payment dates, or deduct a fee automatically. Conditional requirements depend on the actual claim, not just the broad OPD label.

## Monitoring workbook observations

The monitoring sheet uses DATE SENT, NAME, PROVIDER, AGENT, CHANNEL, LACKINGS, STATUS, IN WORDS, and DATE OF DISBURSEMENT. Some actual payment amounts are embedded in text such as `RECEIVED (amount)`; other received entries omit an amount. Some rows also have payment-advice links in an unlabeled column. Future import must flag ambiguous/missing amounts and inconsistent dates rather than assume the full incurred amount was paid. AGENT is not implemented as assignment.

## Email example

The provided screenshot addresses multiple recipients and introduces the applicant's reimbursement request, mentions attached processing documents, offers contact for questions, and includes an RMC2 sign-off. The new default template follows that structure, with fictional addresses and a generic signature, plus a stable request ID and availment details. It does not copy personal names, real recipients, or the signature image into the repository.

The example has one PDF attachment; the prototype supports separate attachments and does not claim to merge images into a PDF. Payment confirmation is a distinct email scenario. Approved amount and actual amount reimbursed remain separate.

## Verification

Checked the full sample path from submission through attachment checks, multi-recipient email, approval, and RMC2 payment; missing/conditional requirements, financial difference notes, CSV fields, mobile layout, enlarged text, and preserved comparison versions. All messages and file previews remain simulations. Live Google permissions, original file retrieval, sending, and incoming-email matching remain future integration work.
