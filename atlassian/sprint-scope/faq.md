---
title: Limits and FAQ
parent: Sprint Scope for Jira
grand_parent: Atlassian
nav_order: 4
---

# Limits and FAQ

## Limits

| Limit | Value |
|---|---|
| Results per function | 1,000 work items. Atlassian sets this limit for JQL functions, and it applies before any other conditions in the query. |
| Sprint size | Up to 20,000 work items checked per sprint: the work currently in it plus recently changed work on its board. |
| Sprints | Active and closed sprints. A future sprint has no scope to report yet. |
| History | Sprint membership only. Status, estimate and other changes aren't tracked. |

## FAQ

### Do the results match the sprint report?

Yes. They use the same rules: work taken out and put back counts as neither added nor removed, and unfinished work carried over to the next sprint isn't counted as removed. See [the exact rules](../jql-functions/#the-exact-rules).

### Can people see work items they otherwise couldn't?

No. Jira applies each person's own permissions to the results, including issue security levels.

### Does it need any setup?

No. After installing, the three functions work for every sprint on the site.

### Does it work in Basic search mode?

No. Jira's Basic mode can't show JQL functions. Use **JQL** mode.

### Can it tell me whether work was finished by the end of the sprint?

Not yet. The functions track which work was in the sprint, not its status at the time. A condition such as `statusCategory = Done` uses each work item's current status.

### How quickly do results update?

Usually within about 10 seconds of a change. See [How fresh are the results?](../jql-functions/#how-fresh-are-the-results)

### What does the app find if work left the sprint without passing through its board?

The app looks for work that left a sprint among the work on the sprint's board. If a work item outside the board's filter was added to the sprint and removed again, it isn't counted. Anything currently in the sprint is always counted.

### What happens if I uninstall the app?

Your sprints and work items are untouched. Saved filters and boards that use the functions stop working, because the functions belong to the app. The app's stored data is removed.

### Something isn't working

Email [support@benchwren.com](mailto:support@benchwren.com). The [Support](/support/) page lists what to include.
