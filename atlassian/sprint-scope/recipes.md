---
title: Sprint review recipes
parent: Sprint Scope for Jira
grand_parent: Atlassian
nav_order: 3
---

# Sprint review recipes

Ready-made searches for sprint reviews, retrospectives and dashboards. Replace `37` with your sprint's id or `"name"`.

## All scope change

Everything that joined or left the sprint after it started:

```
issue in addedAfterSprintStart(37) OR issue in removedAfterSprintStart(37)
```

## Unplanned work

Work the team took on mid-sprint:

```
issue in addedAfterSprintStart(37) AND issue not in removedAfterSprintStart(37)
```

Only the bugs:

```
issue in addedAfterSprintStart(37) AND type = Bug
```

## Dropped scope

Committed work that was taken out of the sprint:

```
issue in inSprintAtStart(37) AND issue in removedAfterSprintStart(37)
```

## Committed and still in the sprint

The original plan, minus anything dropped:

```
issue in inSprintAtStart(37) AND issue not in removedAfterSprintStart(37)
```

Add `AND statusCategory != Done` to see committed work that isn't finished. That uses each work item's current status, so check it at the end of the sprint for an accurate picture.

## Two sprints at once

Each function takes one sprint. Join them with `OR`:

```
issue in addedAfterSprintStart(36) OR issue in addedAfterSprintStart(37)
```

## Put it on a dashboard

1. Run one of the searches above and choose **Save filter**.
2. On a dashboard, add the **Filter results** gadget and pick the saved filter.

Saved results update on their own within about 10 seconds of a change, so the gadget stays current during the sprint.
