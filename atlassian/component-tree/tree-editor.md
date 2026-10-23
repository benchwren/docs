---
title: Tree editor
parent: Component Tree for Jira
grand_parent: Atlassian
nav_order: 2
---

# Tree editor

The editor lives in **Space settings → Component tree**. Only space admins and Jira admins see it, because Jira shows space settings to admins only.

## Moving components

**With the mouse:** drag a component by its row.

- Drop it **between** two rows to change the order.
- Drop it **onto** a row to put it underneath that component.
- Drag it to the left, below its parent, to move it back out a level.

**With the keyboard:** tab to a component's **⋯** button (its label reads "Actions for *name*") and press Enter. The menu offers:

- **Move up** and **Move down**: change the order among siblings.
- **Move to top level**: take it out of its parent.
- **Move under**: pick a new parent from the list. Only valid parents are listed, so you can't place a component under itself or its own children.

Focus stays on the component you moved. Use the arrow next to a component to collapse or expand its children.

## Saving

Every change saves on its own. The title shows **Saving…**, then **Saved**. If a save fails, the tree goes back to how it was and a message explains why.

If two admins edit the same tree at once, the second one sees *"Someone else changed the tree. Reloaded the latest version."* and the editor reloads with the other person's change. Nothing is merged silently.

## When components change in Jira

- **New component:** it appears at the top level of the tree.
- **Renamed component:** it keeps its place. Saved filters that use the old name keep working (see [Branch search](../branch-search/#renames-and-deletes)).
- **Deleted component:** its children move up one level, to the deleted component's parent.

## Import and export as CSV

Open **Import or export as CSV** under the tree.

- **Show CSV export** gives you the current tree as text you can copy into a spreadsheet.
- To import, paste CSV with the header `component,parent` and choose **Import CSV**. Each row names a component and its parent. Leave `parent` empty for a top-level component.

```
component,parent
Platform,
Auth,Platform
Payments,Platform
Refunds,Payments
```

Components are matched by name. Names that don't exist in the space are skipped and listed after the import. The import doesn't create components; add them in Jira first.

## Limits

- A tree can be at most **6 levels** deep.
- Read-only users see the tree but can't drag rows, and get no ⋯ menus or CSV panel.
