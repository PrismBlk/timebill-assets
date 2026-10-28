# TimeBill — User Guide

Turn your team's Jira worklogs into client invoices. TimeBill runs entirely on Atlassian Forge — no external accounts, your data never leaves your Atlassian site.

## Getting started

### 1. Open the configuration page

Open any Jira project → **TimeBill Configuration** in the project sidebar (under Apps).

### 2. Add customers

**Customers tab → + Add Customer**

- **Customer name** — who you bill
- **Default rate** — hourly rate applied to all team members without a custom rate
- **Currency** — USD, EUR, GBP, CNY, JPY, AUD
- **Project keys** — comma-separated Jira project keys whose worklogs bill to this customer (e.g. `PROJ, WEB`)

### 3. Set custom rates (optional)

**Rates tab → + Add Rate**

Pick a team member from the list, set their hourly rate and role (Standard / Senior / Junior / Lead). Custom rates override the customer's default rate for that person.

### 4. Generate invoices

**Invoices tab → + Generate Invoice**

Pick a customer and billing period (defaults to last month). TimeBill:

1. Finds all issues with logged time in that customer's projects
2. Pulls every worklog in the period
3. Applies each member's rate (custom or default)
4. Produces a draft invoice with full line-item detail

Click **View** on any invoice to see line items, subtotals by team member and by project, and to **export CSV** for your accounting workflow.

### 5. Monthly automation

On the 1st of each month, TimeBill automatically drafts invoices for the previous month for every customer. Existing invoices (e.g. manually generated) are never overwritten.

## Dashboard gadget

Add the **TimeBill: Billing Overview** gadget to any dashboard for at-a-glance customer counts, invoice totals, and outstanding amounts, plus one-click invoice generation.

## FAQ

**Where is my data stored?** Customer configs, rates, and invoice drafts are stored in Atlassian Forge storage, scoped to your site. Nothing is sent to third parties.

**Can I edit worklogs from TimeBill?** No. TimeBill is read-only against Jira — it never modifies your issues or worklogs.

**How are hours rounded?** Amounts are rounded to the nearest cent per line item.

## Support

Questions or issues: **prismblk@gmail.com**
