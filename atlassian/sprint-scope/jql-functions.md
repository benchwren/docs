---
title: JQL functions
parent: Sprint Scope for Jira
grand_parent: Atlassian
nav_order: 1
---

# JQL functions

```
issue in inSprintAtStart("Sprint 5")
issue in addedAfterSprintStart("Sprint 5")
issue in removedAfterSprintStart("Sprint 5")
```

Each function takes one argument: a sprint's **name** or its **id**. Use them with `in` or `not in`.

## Naming the sprint

- **By name:** `addedAfterSprintStart("Sprint 5")`. Upper and lower case don't matter. If several sprints on the site share the name, the function asks you to use the id instead.
- **By id:** `addedAfterSprintStart(37)`. Open the sprint's **Sprint burndown** report from the board's **Reports** page. The id is the number after `sprint=` in the page address.

An id always means the same sprint, even if someone renames it later. Prefer ids in saved filters and boards.

## Examples

Everything added after the sprint started:

```
issue in addedAfterSprintStart("Sprint 5")
```

Added work that isn't finished yet:

```
issue in addedAfterSprintStart("Sprint 5") AND statusCategory != Done
```

The committed scope, minus anything taken out:

```
issue in inSprintAtStart("Sprint 5") AND issue not in removedAfterSprintStart("Sprint 5")
```

Bugs that were added mid-sprint:

```
issue in addedAfterSprintStart(37) AND type = Bug
```

## The exact rules

The functions follow Jira's sprint report:

- **The start** is the sprint's start date. If the team changes the start date when it starts the sprint, that date is the line.
- **Added** means the work item came into the sprint after the start: moved in, or created straight into the sprint.
- **Removed** means the work item was in the sprint at some point after the start, and was out of it when the sprint closed. For an active sprint, it means out of the sprint now.
- A work item taken out and put back again counts as **neither** added nor removed.
- Unfinished work that moves on to the next sprint when the sprint closes is **not** counted as removed.
- Changes made after a sprint closed are ignored.

A sprint that hasn't started yet has no scope to report. The functions show an error for it.

## How fresh are the results?

Jira saves the result of a JQL function and reuses it. The app updates saved results automatically, usually within about 10 seconds, when:

- a work item's Sprint field changes, or a work item is created into a sprint;
- a sprint is started, edited or closed.

A bulk move of many work items causes just one update.

## Error messages

| Message | What to do |
|---|---|
| Sprint "…" was not found or has not started | Check the name or id. A future sprint has no scope yet. |
| More than one sprint is named "…" | Use the sprint's id. |
| More than 1,000 work items match | Narrow the query, or see [Limits](../faq/#limits). |
| Sprint "…" has too many work items for this app to check in one go | See [Limits](../faq/#limits). |
