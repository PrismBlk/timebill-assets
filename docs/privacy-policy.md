# Privacy Policy — TimeBill

> Last updated: 2026-10-27

TimeBill ("the app") is an Atlassian Forge app that turns Jira worklogs into client billing summaries. This policy explains what data the app processes and how.

## What the app reads

When you use TimeBill, the app reads — through Atlassian's official APIs, within your own Atlassian site:

- **Jira worklogs**: time spent entries, the author (display name and account ID), start date, and the issue/project they belong to. This is the sole input for invoice calculations.
- **Jira user directory** (display name and account ID) — only to populate the rate-configuration dropdown.
- **Project keys and issue summaries** — to label invoice line items.

Access is read-only. The app never modifies, creates, or deletes your Jira issues or worklogs.

## What the app stores

Configuration and generated invoices are stored in **Atlassian Forge storage (KVS)**, hosted by Atlassian inside the Forge platform, scoped to your site's installation:

- Customer configurations (name, default hourly rate, currency, mapped project keys)
- Per-user billing rates (user account ID, rate, role label, display name)
- Generated invoice drafts (aggregated line items: user, issue key, hours, rate, amount)

This data never leaves the Atlassian Forge platform. We have no separate database, no analytics, no third-party services, and no servers of our own.

## Personal data declaration

The app stores Atlassian user references (account IDs) and display names as part of rate configuration and invoice line items, for as long as the configuration or invoice exists. Uninstalling the app deletes all associated Forge storage.

## Permissions

The app requests the minimum Atlassian scopes required:

- `read:jira-work` — read issues and worklogs
- `read:jira-user` — read user names for the rate dropdown
- `storage:app` — store your configurations and invoices in Forge storage

No write access to Jira, no admin permissions, no external network calls.

## Contact

Questions about this policy: prismblk@gmail.com
