---
title: Limits and FAQ
parent: Sprint Scope for Jira
grand_parent: Atlassian
nav_order: 2
---

# Limits and FAQ

## Limits

| Limit | Value |
|---|---|
| Results per function | Up to 1,000 matching work items. That's a limit Atlassian sets for JQL functions. |
| Work items checked per sprint | Up to 20,000, counting work items currently in the sprint and recently updated ones on its board. |
| Where history is read from | The sprint's board. A work item that isn't on the board, and was added to the sprint and removed again, is missed. Anything currently in the sprint is always found. |

## FAQ

### Do the results match the sprint report?

Yes. The rules are the same: work taken out and put back counts as neither added nor removed, and unfinished work carried over to the next sprint isn't counted as removed. See [the exact rules](../jql-functions/#the-exact-rules).

### Can people see work items they otherwise couldn't?

No. Jira applies each person's own permissions to the results, including issue security levels.

### Do I need to set anything up?

No. After installing, the three functions work on every board on the site.

### How quickly do results update?

Usually within about 10 seconds of a change to a sprint or to a work item's Sprint field. See [How fresh are the results?](../jql-functions/#how-fresh-are-the-results)

### What happens if I uninstall the app?

Your sprints and work items are untouched. Saved filters and boards that use the functions stop working, because the functions belong to the app. The app's stored data is removed.

### Something isn't working

Email [support@benchwren.com](mailto:support@benchwren.com). The [Support](/support/) page lists what to include.
