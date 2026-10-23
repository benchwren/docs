---
title: Data and security
parent: Component Tree for Jira
grand_parent: Atlassian
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

Before it reads or changes anything, the app checks the permissions of the person using it, as that person. Viewing needs permission to browse the space. Changing the tree needs space admin or Jira admin rights. Branch browser counts run as the person viewing them. Background updates, such as refreshing saved filters and path values, run as the app. Atlassian normally grants this access automatically; if Jira shows an "Allow access" prompt, accepting it once is enough.

## Who can change what

- Only space admins and Jira admins can change the tree, from the space settings page Jira shows only to admins. Every change is checked again on the server.
- Everyone who can see the space can use `componentBranch` and the branch browser.

## Known limits

- **Error messages.** A `componentBranch` query that names a space or component that doesn't exist returns an error saying so. That error can confirm whether a space key or component name exists.

## Privacy

How Benchwren handles personal data, including app logs, licence contacts and support email, is described in the [Privacy policy](/legal/privacy/).

## Removing data

When an admin uninstalls the app, Atlassian removes the app's Forge storage under its data retention rules for Forge apps. Jira's components and work items are not changed.
