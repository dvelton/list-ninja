# List Ninja

A tool that generates SharePoint List integration kits for AI coding tools. You describe your SharePoint list, and List Ninja produces a complete reference document that AI tools like Cursor, Claude, GitHub Copilot, or Lovable can use to build a working web app backed by your list.

No sign-ups, no accounts, no installations. Open the HTML file in your browser, fill in your list details, and copy the output.

## What problem does this solve?

Building an app on top of a SharePoint List means dealing with API endpoints, field naming conventions, request headers, and deployment details. AI coding tools can handle all of this — but only if you give them the right context. Manually writing that context is tedious and easy to get wrong.

List Ninja automates the tedious part. You enter your list's URL and column schema, and it generates a structured reference document that tells the AI tool exactly how to talk to your list.

## How to use it

1. Open `index.html` in your browser (works locally — no server needed)
2. Paste your SharePoint List URL (e.g., `https://contoso.sharepoint.com/sites/Marketing/Lists/CampaignTracker`)
3. Define your columns: enter the display name, internal field name, and type for each column
4. Pick an output format (Generic Markdown, Cursor, Claude, or GitHub Copilot)
5. Click **Generate Kit**
6. Copy the output and paste it into your AI coding tool

The generated kit includes:
- A plain-English explanation of how to use it (suitable for non-technical users)
- Ready-to-use JavaScript helper functions for reading and writing list data
- Every API endpoint your app needs, with your actual field names filled in
- A column schema reference table
- A pre-written AI system prompt that tells the tool exactly how to work with your list
- Step-by-step deployment instructions for uploading your finished app to SharePoint

## How the generated apps work

Apps built from a List Ninja kit are designed to run directly on your SharePoint site. You upload the HTML file to a document library (like Site Assets), and it runs in your browser with full access to your list data.

Authentication is automatic — because the app lives on the same SharePoint site as your list, your existing SharePoint login handles everything. No app registration, no tokens, no IT department involvement.

The one requirement: your SharePoint site needs "custom script" enabled. This is a site-level setting (not a global IT policy). The generated kit explains how to check this and what to do if it's turned off.

## Features

- **Multiple lists**: Use the tab interface to define multiple SharePoint lists for apps that need more than one data source
- **Multiple output formats**: Generate kits formatted for Cursor (.cursorrules), Claude (project instructions), GitHub Copilot (AGENTS.md), or generic Markdown
- **Section-level copying**: Copy individual sections (endpoints, schema, system prompt, etc.) instead of the whole kit
- **Live URL parsing**: See your SharePoint URL broken down into its components as you type
- **Column type support**: Text, Number, Choice, DateTime, Boolean, Person, and Lookup fields

## Requirements

A web browser. That's it. List Ninja is a single HTML file with no external dependencies.

## License

MIT
