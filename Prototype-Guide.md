# RMC2 reimbursement prototype

This prototype uses fictional people, documents, and messages. No Google account is connected, and no real email can be sent. Reloading or resetting restores the sample data.

## Start on Home

Home answers “What needs to be done?” Each request has one main action: check documents, check missing files, read a reply, or send a follow-up. Overdue follow-ups appear first.

Use **All requests** to search by name/reference, status, or received-date range. **Emails** shows the selected demo account’s messages. Other tools remain under **More tools**.

## Try the whole flow

1. On Home, choose **Add sample request**, then submit the sample form.
2. Choose **Documents**. Open each file and choose **File is clear — mark checked**. The next unchecked file opens automatically. Flag unclear files for replacement if needed.
3. Select the files to include, then choose **2. Prepare email**. Check the recipient, message, and attachments. Choose **Send demo email**.
4. In the request’s Emails tab, expand **Try a sample department reply** and add a fictional reply.
5. Read the response and confirm the suggested decision where appropriate.
6. Under **Details → Update status**, a Paid status requires a payment date and a reason. **History** shows timestamped activity.

## Dates

The sample clock begins on **6 October 2026, 10:30 am, Asia/Manila**. This fixed demo date keeps overdue examples reproducible; it is not a live clock.

Received, updated, sent, last-reply, follow-up, treatment, and payment dates have separate meanings. Sending schedules a reminder three calendar days later in this prototype. Set or remove the reminder using **Set follow-up date**. Dates are included in the CSV download. Business-day scheduling is not implemented in this demo.

## Other controls

- Switch between Alex and Sam in the sidebar to explore separate simulated Gmail accounts. This is not authentication or assignment.
- Match an unmatched email to a request in Emails.
- Save and reopen the current demo draft. One active draft is supported.
- Change demo recipients/templates in Settings; add notes; download sample records.

## Downloaded copy

Extract `RMC2-Prototype.zip` and open `index.html`. Keep all JavaScript, CSS, and logo files beside it.

Validation included the document-review gate, send/reply/payment flow, future and due reminders, timestamped history, inclusive date filtering, mobile layout, and 200% text enlargement. Optional WebMCP remains feature-detected; no native supported testing context was available. The design still needs usability feedback from its intended users before production development.
