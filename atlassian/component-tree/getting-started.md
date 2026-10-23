---
title: Getting started
parent: Component Tree for Jira
grand_parent: Atlassian
nav_order: 1
---

# Getting started

You need to be a **space admin** (project admin) or a **Jira admin** to arrange the tree. Everyone else can search with it and see it read-only.

## 1. Open the tree editor

In a company-managed space, go to **Space settings → Component tree**.

Every existing component appears at the top level. If the space has no components yet, add them first in **Space settings → Components**, then come back.

## 2. Arrange the tree

Drag a component onto another one to put it underneath. Or open a component's **⋯** menu and choose **Move under**, then the parent you want. Changes save automatically; you'll see **Saved** next to the title.

See [Tree editor](../tree-editor/) for all the ways to move components, and for importing a whole tree from CSV.

## 3. Search a branch

Use the `componentBranch` function in JQL to find work items in a component **or anywhere under it**:

```
component in componentBranch("KEY", "Platform")
```

Replace `KEY` with your space key and `Platform` with a component name. The editor shows a ready-made example with a **Copy** button. Save it as a filter and build a board from it if you like. When the tree changes, saved filters and boards follow within about a minute.

## Optional: show the path on work items

To show the **Component path** field (for example `Platform / Payments / Refunds`) on work items, add it to the screens of your work types once. See [Component path field](../component-path/).
