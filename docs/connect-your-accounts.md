# Connect your accounts

[Back to the main page](../README.md)

The templates ship with no accounts attached. After importing, you connect your own once, and n8n remembers them for every workflow.

| Account | Used by | Cost |
|---|---|---|
| Google Sheets | All three templates | Free |
| Gmail | All three templates | Free |
| Google Calendar | AI Voice Receptionist | Free |
| Google Gemini | Lead Follow-up, Customer Re-engagement | Free tier |

## Google Sheets, Gmail and Google Calendar

### On n8n Cloud

1. Open any node that shows a warning, for example **Read Leads**.
2. Under **Credential to connect with**, choose **Create new credential**.
3. Click **Sign in with Google** and allow access with the Google account you want to use.
4. Do the same once for Gmail (open **Send Email**) and, for the voice receptionist, Google Calendar (open **Read Calendar**).
5. Open every other Google node and pick the credential you just made from the list.

The Gmail account you connect is the one the emails are sent from.

### On self-hosted n8n

Self-hosted n8n needs your own Google OAuth app. This is free and takes about 15 minutes.

1. In the [Google Cloud Console](https://console.cloud.google.com), create a project.
2. Enable these APIs: **Gmail API**, **Google Sheets API**, **Google Drive API** and, for the voice receptionist, **Google Calendar API**.
3. Set up the **OAuth consent screen** and add your own Google account as a test user.
4. Create an **OAuth client ID** of type **Web application**. Paste the **OAuth Redirect URL** shown in the n8n credential window into **Authorized redirect URIs**.
5. Copy the **Client ID** and **Client Secret** into the n8n credential and click **Sign in with Google**.

The full guide with screenshots is in the [n8n documentation](https://docs.n8n.io/integrations/builtin/credentials/google/oauth-single-service/).

## Google Gemini (free)

1. Go to [Google AI Studio](https://aistudio.google.com) and sign in.
2. Click **Get API key**, then **Create API key**. Copy it.
3. In n8n, open the **Gemini (free tier)** node.
4. Under **Credential to connect with**, choose **Create new credential**, paste the key into **API Key**, leave the host as it is, and save.

The free tier has daily and per-minute limits. For a small business sending up to a few dozen emails a day, that is plenty. If the limit is reached, the workflow sends the built-in template instead, so nothing is missed.

Do not want AI at all? Set `useAI` to `false` in **Your Settings**. The Gemini node can then stay unconnected.

## Connect your Google Sheet

Every template reads from and writes to a Google Sheet. The exact tabs and headers are in each template's guide.

1. Create the sheet with the headers from the guide (row 1).
2. Copy the sheet's URL from your browser's address bar.
3. Open each Google Sheets node in the workflow. Under **Document**, choose **By URL** and paste the link.

## Check before you go live

- Every node with a warning icon has a credential selected.
- **Your Settings** is filled in with your real details.
- A test run with your own email address worked.
