# Gmail → Claude AI → Google Sheets Automation (n8n)

An n8n workflow that automatically extracts and logs email data using Claude AI.

## What it does

- Monitors Gmail for new incoming emails
- Sends email content to Claude (Anthropic API) for intelligent extraction
- Parses and structures the extracted data
- Appends a new row to Google Sheets with the extracted fields
- Sends a confirmation email when data is successfully logged

## Workflow

Gmail Trigger → HTTP Request (Claude API) → Code (parse JSON) → Google Sheets (append) → Gmail (send confirmation)

## Fields Extracted

- Sender
- Subject
- Date
- Summary
- Action Items

## Tech Stack

- n8n (workflow automation)
- Anthropic Claude API (claude-sonnet-4-6)
- Gmail API (OAuth)
- Google Sheets API
- JavaScript (Code node for JSON parsing)

## Use Cases

- Email triage and logging
- Automating data entry from inbound emails
- AI-powered inbox summarization
- Client communication tracking

## Setup

1. Import the workflow JSON into your n8n instance
2. Set up Gmail OAuth credentials
3. Set up Google Sheets OAuth credentials
4. Add your Anthropic API key in the HTTP Request node headers
5. Create a Google Sheet with columns: sender, subject, date, summary, action_items
6. Activate the workflow
