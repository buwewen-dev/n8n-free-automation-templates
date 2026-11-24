# How to download the templates

[Back to the main page](../README.md)

You only need the `.json` file of each template. Pick whichever way is easiest for you.

## Option 1: Download everything as a ZIP (easiest)

1. Go to the main page of this repository: https://github.com/buwewen-dev/n8n-free-automation-templates
2. Click the green **Code** button near the top right.
3. Click **Download ZIP**.
4. Unzip the file on your computer. The workflows are inside the `templates` folder:
   - `templates/lead-follow-up/lead-follow-up.json`
   - `templates/customer-re-engagement/customer-re-engagement.json`
   - `templates/ai-voice-receptionist/ai-voice-receptionist.json`

## Option 2: Download one template

1. Open the template's folder, for example `templates/lead-follow-up`.
2. Click the `.json` file.
3. Click the **Download raw file** button (the arrow pointing down, at the top right of the file).

## Option 3: Import straight from the link (no download)

n8n can import a workflow from a URL.

1. In n8n, open a new workflow.
2. Click the **...** menu at the top right and choose **Import from URL**.
3. Paste the raw link of the template:

   | Template | Raw link |
   |---|---|
   | Lead Follow-up System | `https://raw.githubusercontent.com/buwewen-dev/n8n-free-automation-templates/main/templates/lead-follow-up/lead-follow-up.json` |
   | Customer Re-engagement | `https://raw.githubusercontent.com/buwewen-dev/n8n-free-automation-templates/main/templates/customer-re-engagement/customer-re-engagement.json` |
   | AI Voice Receptionist | `https://raw.githubusercontent.com/buwewen-dev/n8n-free-automation-templates/main/templates/ai-voice-receptionist/ai-voice-receptionist.json` |

## Import the file into n8n

1. In n8n, click **Create workflow** (or the **+** button).
2. Click the **...** menu at the top right of the editor.
3. Choose **Import from File** and pick the `.json` file you downloaded.
4. The workflow appears on the canvas. Click **Save**.

Some nodes will show a warning icon at first. That is normal: they are waiting for you to connect your own accounts. Next step: [Connect your accounts](connect-your-accounts.md).
