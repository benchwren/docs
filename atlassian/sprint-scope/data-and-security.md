---
title: Data and security
parent: Sprint Scope for Jira
grand_parent: Atlassian
nav_order: 3
---

# Data and security

Sprint Scope for Jira is built on Atlassian Forge and is eligible for Atlassian's **Runs on Atlassian** program: it runs entirely on Atlassian's cloud and sends no data to any outside server.

## Where data lives

| Data | Where it's stored |
|---|---|
| For each sprint the functions have been used on: the ids and creation dates of the work items that were in it, and when it was last checked | Forge storage, in Atlassian's cloud, separate for each Jira site |
| When each sprint's saved results were last updated | Forge storage |
| Saved function results (lists of work item ids) | Jira itself, which stores the results of JQL functions |

The app doesn't store work item content, comments, attachments or anything about users. Benchwren has no servers and can't see your data.

## Permissions the app asks for

| Scope | Why |
|---|---|
| `read:jira-work` | Read work items and the Sprint field's history |
| `read:sprint:jira-software` | Read sprints and their start and close dates |
| `read:board-scope:jira-software`, `read:board-scope.admin:jira-software` | Read a sprint's board and the filter behind it, to find work items that moved in or out |
| `read:project:jira` | Required by Jira's board APIs |
| `storage:app` | Keep the per-sprint data above in Forge storage |
| `read:app-data:jira`, `write:app-data:jira` | Keep Jira's saved function results up to date |

The app only reads Jira. It never changes work items, sprints or boards.

The functions read sprint history as the app, because Jira asks the app for one result that many people's searches share. Jira then applies each person's own permissions to that result, so nobody sees a work item they couldn't already see.

## Known limits

- **Error messages.** The messages for a sprint name shared by several sprints, or for a sprint that's too large, can confirm that a sprint with that name or id exists. They never show the sprint's work items.

## Privacy

How Benchwren handles personal data, including app logs, licence contacts and support email, is described in the [Privacy policy](/legal/privacy/).

## Removing data

When an admin uninstalls the app, Atlassian removes the app's Forge storage under its data retention rules for Forge apps. Sprints and work items are not changed.
