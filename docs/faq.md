# FAQ

[Back to the main page](../README.md)

## Is it really free?

Yes. The templates are free under the MIT license. The tools they use all have free tiers: n8n (self-hosted is free, n8n Cloud has a trial), Google Sheets, Gmail, Google Calendar and the Gemini API. The voice receptionist needs a voice platform (ElevenLabs, Vapi or Retell), which charges per call minute after its free credits.

## Can I sell the setup to clients?

Yes. That is the point. See [Selling these to clients](selling-to-clients.md).

## How many emails can I send per day?

Gmail limits you to about 500 emails a day on a free account and about 2,000 on Google Workspace. The `dailyLimit` setting (default 20 per run) keeps you far below that. Raise it slowly if you need more.

## Will my emails land in spam?

The emails are short, plain text and sent from your own Gmail, which is the best case for deliverability. Keep the daily limit modest, use a real name in `yourName`, and do not add links to unknown sites.

## The workflow ran but nobody got an email. Why?

Check these in order:

1. **Status column.** Only leads with an empty status, `New` or `Contacted` are emailed (or customers without `Stop`, `Unsubscribed` or `Replied`).
2. **Dates.** For re-engagement, the `Last Visit` must be at least 30 days ago and written as a date, like `2026-10-01`.
3. **Email column.** The address must be valid.
4. **Headers.** Row 1 must match the guide exactly, including capitals and spaces.
5. **Executions.** Open the **Executions** tab in n8n and click the last run to see what each node did.

## Can I use Outlook instead of Gmail?

Yes. Replace the Gmail nodes with the Microsoft Outlook nodes and keep the same fields (to, subject, message). The reply check uses Gmail search, so you would swap that node too.

## Can I use a different AI model?

Yes. Replace the **Gemini (free tier)** node with any chat model node in n8n (OpenAI, Anthropic, Mistral, a local model with Ollama). The rest of the workflow stays the same.

## Can I use Airtable or a CRM instead of Google Sheets?

Yes. Replace the Google Sheets nodes with the Airtable or CRM nodes and keep the same column names.

## What time does it run?

The email templates run every morning (9:00 and 10:00). Change the time in the first node, and set your time zone under **Workflow settings** (it starts as America/New_York).

## Where do I report a problem?

Open an issue on this repository with a screenshot of the failing node (hide any personal data first).
