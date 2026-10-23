---
title: Component path field
parent: Component Tree for Jira
grand_parent: Atlassian
nav_order: 4
---

# Component path field

**Component path** is a read-only field that shows where a work item's components sit in the tree, for example:

```
Platform / Payments / Refunds
```

If a work item has more than one component, the paths are separated by a semicolon: `Platform / Auth; Platform / Payments`.

## It updates by itself

The app keeps the field up to date in the background. When someone changes a work item's components, or an admin moves, renames or deletes a component, the affected work items update without anyone opening them, usually within a minute.

## Show it on work items

Jira shows a field only after it's on the work type's screen. A space admin does this once for each work type:

| Space type | Where |
|---|---|
| Software | Space settings → Work items → Screens |
| Service | Space settings → Request management → Screens |
| Business | Space settings → Screens |

Open each screen in use, add **Component path**, and save. Jira then shows it in the work item view, usually under **Context fields**.

To find work items in a branch, use [`componentBranch`](../branch-search/) rather than the path field.

## Limits

- The field is limited to **255 characters**. Longer paths are cut short and end with "…". Jira's own views may shorten long text further; open the work item to see the full value.
- It's read-only. Change the components or the tree, not the field.
