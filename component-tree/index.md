---
title: Component Tree for Jira
nav_order: 2
has_children: true
permalink: /component-tree/
---

# Component Tree for Jira

Jira components are a flat list. Real products aren't: a *Payments* area has *Refunds* and *Checkout* inside it, and *Platform* holds *Auth* and *Payments*. Component Tree lets you arrange your existing components into a tree, without adding a new field or changing how people pick components.

## What you get

| Feature | What it does |
|---|---|
| **Tree editor** | Arrange components into parents and children by drag and drop or with the keyboard. Space settings → Component tree. |
| **Branch search** | A JQL function, `componentBranch`, that matches a component and every component under it. Works in saved filters and boards. |
| **Component path field** | A read-only field that shows each work item's full path, such as `Platform / Payments / Refunds`. It updates by itself. |
| **Branch browser** | A space page that shows the tree with work item counts for each branch, and opens a search for any branch. |

## How it fits with Jira

- Jira's own **Components** field stays the source of truth. People keep picking components exactly as before; the app only adds the structure around them.
- The app works in **company-managed** spaces of any type (software, service and business). Team-managed spaces don't have components, so there's nothing to arrange there.
- It runs entirely on Atlassian's cloud (Forge, *Runs on Atlassian*). See [Data and security](data-and-security/).

## Start here

1. [Getting started](getting-started/): build your first tree in three steps.
2. [Tree editor](tree-editor/): every way to move components, plus CSV import and export.
3. [Branch search](branch-search/): the `componentBranch` JQL function.
4. [Component path field](component-path/): show the path on work items.
5. [Branch browser](branch-browser/): counts per branch.
6. [Limits and FAQ](faq/).
