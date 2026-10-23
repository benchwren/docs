---
title: Limits and FAQ
parent: Component Tree for Jira
grand_parent: Atlassian
nav_order: 6
---

# Limits and FAQ

## Limits

| Limit | Value |
|---|---|
| Tree depth | 6 levels |
| Component path field | 255 characters, longer values end with "…" |
| Space types | Company-managed spaces (software, service, business). Team-managed spaces have no components. |
| Scope | One tree per space. A tree can't span several spaces. |

## FAQ

### Does it change the Components field?

No. Jira's own Components field stays exactly as it is, and people keep picking components the same way. The app adds structure around it and never adds a second "components" field.

### Who can change the tree?

Space admins and Jira admins, from **Space settings → Component tree**. Everyone else sees it read-only, in the branch browser and in the settings page if they can open it.

### Do users need to grant the app access?

Usually not. The app checks your permissions and counts work items as you, so it never shows you more than you can already see. Atlassian normally grants that access automatically. If Jira ever shows an **Allow access** prompt, accept it once and the app will load.

### How fast do filters, boards and paths update after I move a component?

Usually within a minute. Saved filters and boards often update within seconds; the Component path field on many work items can take a little longer.

### What happens if I uninstall the app?

Jira's components and work items are untouched. Saved filters that use `componentBranch` stop working, because the function belongs to the app, and the Component path field stops updating. The stored tree is removed with the app's data.

### Do the counts respect issue security?

Yes. The branch browser counts work items as you, so work items hidden from you by an issue security scheme aren't counted.

### Something isn't working

Email [support@benchwren.com](mailto:support@benchwren.com). The [Support](/support/) page lists what to include.
