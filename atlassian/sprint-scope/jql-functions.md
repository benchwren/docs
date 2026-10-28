---
title: JQL functions
parent: Sprint Scope for Jira
grand_parent: Atlassian
nav_order: 2
---

# JQL functions

```
issue in inSprintAtStart("Sprint 14")
issue in addedAfterSprintStart("Sprint 14")
issue in removedAfterSprintStart("Sprint 14")
```

Each function takes one argument, a sprint's name or id (see [Pick a sprint](../getting-started/#1-pick-a-sprint)), and works with `in` and `not in`. Combine them with any other JQL:

```
issue in addedAfterSprintStart(37) AND type = Bug ORDER BY created DESC
```

## `inSprintAtStart`

The work that was in the sprint at the moment it started: the scope the team committed to. It stays the same for the life of the sprint, whatever happens afterwards.

## `addedAfterSprintStart`

Work that joined the sprint after it started, whether it was moved in from the backlog or another sprint, or created straight into the sprint.

## `removedAfterSprintStart`

Work that was in the sprint at some point after it started, and was out of it when the sprint closed. For an active sprint, it's the work that has left so far. This includes work that was added mid-sprint and then taken out again.

## A worked example

Sprint 14 starts on Monday with 20 work items, including PAY-7 and PAY-12. During the sprint:

| Work item | What happened | At start | Added | Removed |
|---|---|:---:|:---:|:---:|
| PAY-7 | Moved to the backlog on Tuesday, back into the sprint on Wednesday | ✓ | | |
| PAY-12 | Moved to the backlog on Wednesday | ✓ | | ✓ |
| PAY-31 | A bug created straight into the sprint on Tuesday | | ✓ | |
| PAY-40 | Moved in on Thursday, moved to the next sprint on Friday | | ✓ | ✓ |
| PAY-18 | Not finished; carried over to Sprint 15 when Sprint 14 closed | ✓ | | |

PAY-7 counts as neither added nor removed, because it ended up where it started. PAY-18 isn't removed, because unfinished work carried over at close still belongs to the sprint, as in Jira's sprint report.

## The exact rules

The functions follow Jira's sprint report:

- **The start** is the sprint's start date. If the team edits the start date when starting the sprint, that date is the line.
- **Added** means the work item joined after the start: moved in, or created straight into the sprint.
- **Removed** means the work item was in the sprint after the start and out of it at close (for an active sprint: out of it now).
- Work taken out and put back counts as **neither** added nor removed.
- Unfinished work carried over to the next sprint at close is **not** removed.
- Changes made after a sprint has closed are ignored.

The functions look at sprint membership only. Conditions such as `statusCategory = Done` use each work item's **current** status, not its status when the sprint closed.

## How fresh are the results?

Jira saves the result of a JQL function and reuses it, which keeps filters and boards fast. The app updates saved results automatically, usually within about 10 seconds, when:

- work moves into or out of a sprint, or is created into one;
- a sprint is started, edited or closed.

A bulk move of many work items causes a single update.

## Error messages

| Message | What it means |
|---|---|
| Sprint "Sprint 9" was not found or has not started | There's no sprint by that name or id, or it hasn't started yet. A future sprint has no scope to report. |
| More than one sprint is named "Sprint 9" | Several sprints on the site share that name. Use the sprint's id instead. |
| More than 1,000 work items match | One function's result is larger than Jira allows. See [Limits](../faq/#limits). |
| Sprint "Sprint 9" has too many work items for this app to check in one go | The sprint is larger than the app can check. See [Limits](../faq/#limits). |
