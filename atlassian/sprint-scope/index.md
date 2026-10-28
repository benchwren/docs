---
title: Sprint Scope for Jira
parent: Atlassian
nav_order: 2
has_children: true
permalink: /atlassian/sprint-scope/
---

# Sprint Scope for Jira

A sprint starts with a plan. By the end, a couple of urgent bugs have been pulled in, a story has been dropped, and someone asks in the review what actually changed. Jira's sprint report shows it, but you can't search it: Jira Cloud rejects `sprint WAS` and `sprint CHANGED`, so you can't filter, export or build a board from scope change.

Sprint Scope adds three JQL functions that make sprint scope change searchable.

## What you get

| Function | Finds |
|---|---|
| **`inSprintAtStart`** | The committed scope: work that was in the sprint when it started. |
| **`addedAfterSprintStart`** | Work that joined the sprint after it started, including work created straight into it. |
| **`removedAfterSprintStart`** | Work that left the sprint before it closed, or, while the sprint is active, has left it so far. |

```
issue in addedAfterSprintStart("Sprint 14")
```

Use them in work item search, saved filters, and anything built on a filter, such as boards and dashboard gadgets. They combine with any other JQL.

## How it fits with Jira

- **Nothing to set up.** Once the app is installed, the functions work for every sprint on the site, for everyone who can search.
- **Same rules as the sprint report.** Work taken out and put back doesn't count as a change, and unfinished work carried over to the next sprint isn't counted as removed.
- **Your permissions still apply.** People only ever see work items they're already allowed to see.
- **Runs on Atlassian.** The app runs entirely on Atlassian's cloud (Forge) and only reads your site. See [Data and security](data-and-security/).

## Start here

1. [Getting started](getting-started/): your first scope-change search in three steps.
2. [JQL functions](jql-functions/): each function, a worked example, and the exact rules.
3. [Sprint review recipes](recipes/): ready-made queries for reviews, retros and dashboards.
4. [Limits and FAQ](faq/).
5. [Data and security](data-and-security/).
