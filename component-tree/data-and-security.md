---
title: Data and security
parent: Component Tree for Jira
nav_order: 7
---

# Data and security

Component Tree for Jira is built on Atlassian Forge and is eligible for Atlassian's **Runs on Atlassian** program: it runs entirely on Atlassian's cloud and sends no data to any outside server.

## Where data lives

| Data | Where it's stored |
|---|---|
| The tree: which component sits under which, and in what order | Forge storage, in Atlassian's cloud, separate for each Jira site |
| A snapshot of component names, and the old names of renamed or deleted components, so saved filters keep working | Forge storage |
| Component path values | A Jira custom field on your work items |

The app doesn't store work item content, comments, attachments or anything about users. Benchwren has no servers and can't see your data.

## Permissions the app asks for

| Scope | Why |
|---|---|
| `read:jira-work` | Read spaces, components and work items to build the tree, answer `componentBranch` queries and compute paths and counts |
| `storage:app` | Keep the tree in Forge storage |
| `read:app-data:jira`, `write:app-data:jira` | Keep saved filters up to date and write the Component path field |

The app acts as itself, never on behalf of individual users.

## Who can change what

- Only space admins and Jira admins can change the tree, from the space settings page Jira shows only to admins. Every change is checked again on the server.
- Everyone who can see the space can use `componentBranch` and the branch browser.

## Known limits

- **Counts and issue security.** Because the app reads as itself, branch browser counts can include work items hidden from the viewer by an issue security scheme. Only the counts are affected; no work item details are shown, and the search a branch link opens respects your permissions.
- **Error messages.** A `componentBranch` query that names a space or component that doesn't exist returns an error saying so. That error can confirm whether a space key or component name exists.

## Removing data

When an admin uninstalls the app, Atlassian removes the app's Forge storage under its data retention rules for Forge apps. Jira's components and work items are not changed.
