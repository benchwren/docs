---
title: Branch browser
parent: Component Tree for Jira
nav_order: 5
---

# Branch browser

The branch browser shows the tree to everyone in the space, with work item counts for each branch.

## Where to find it

It's a space page, so it appears in the space's top tab bar. If you don't see **Component tree** there, look under **More**, or add it with **+**.

## What it shows

- Each component, with its children under it. Expand a component to see the next level.
- For each branch, the number of work items in **To Do**, **In Progress** and **Done**, counting the component and everything under it.
- Click a branch to open a search for all its work items.

Counts load in batches, so a big tree fills in from the top. If counts fail to load, choose **Retry**.

## Notes

- Counts are approximate and meant as a quick overview, not a report.
- The search a branch link opens lists the branch's component names, so it works in Jira's Basic search mode too. It's a snapshot of the branch at the time you click. For a saved filter that follows tree changes, use [`componentBranch`](../branch-search/).
