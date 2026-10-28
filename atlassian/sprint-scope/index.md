---
title: Sprint Scope for Jira
parent: Atlassian
nav_order: 2
has_children: true
permalink: /atlassian/sprint-scope/
---

# Sprint Scope for Jira

Jira Cloud can't search sprint history. Queries such as `sprint WAS "Sprint 5"` or `sprint CHANGED` are rejected, so there's no way to list the work that was added to a sprint after it started, or pulled out of it. The sprint report shows these changes, but you can't filter, export or build a board from it.

Sprint Scope adds three JQL functions that answer exactly those questions.

## What you get

| Function | Finds |
|---|---|
| `issue in inSprintAtStart("Sprint 5")` | Work that was in the sprint when it started: the committed scope |
| `issue in addedAfterSprintStart("Sprint 5")` | Work that came into the sprint after it started, including work created straight into it |
| `issue in removedAfterSprintStart("Sprint 5")` | Work that was in the sprint and was taken out before it closed (or, for an active sprint, isn't in it now) |

They work anywhere Jira takes JQL: issue search, saved filters, boards, dashboards and automation rules. The results follow the same rules as Jira's sprint report.

## How it fits with Jira

- There's nothing to set up. Install the app, and the functions are available on every board on the site.
- Results respect Jira permissions. People see only the work items they're already allowed to see.
- It runs entirely on Atlassian's cloud (Forge, *Runs on Atlassian*). See [Data and security](data-and-security/).

## Start here

1. [JQL functions](jql-functions/): the three functions, with examples and the exact rules.
2. [Limits and FAQ](faq/).
3. [Data and security](data-and-security/).
