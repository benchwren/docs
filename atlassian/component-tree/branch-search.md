---
title: Branch search
parent: Component Tree for Jira
grand_parent: Atlassian
nav_order: 3
---

# Branch search with `componentBranch`

`componentBranch` is a JQL function. It matches a component **and every component under it** in the tree.

```
component in componentBranch("KEY", "Component name")
```

- The first argument is the space key, such as `CT`.
- The second is the component name. Names aren't case-sensitive.

Use `not in` to exclude a whole branch:

```
component not in componentBranch("KEY", "Payments")
```

You can combine it with any other JQL, for example:

```
component in componentBranch("KEY", "Platform") AND statusCategory != Done ORDER BY priority DESC
```

## Use it in filters and boards

Type the query in **JQL** mode of the search page, then save it as a filter. Boards built from that filter show the whole branch. When you change the tree, saved filters and boards pick up the change on their own, usually within a minute.

Jira's **Basic** search mode can't show a JQL function inside its Components picker. Use JQL mode for queries that use `componentBranch`.

## Renames and deletes

- **Rename:** if you rename `Payments` to `Payments Core`, a saved filter that still says `componentBranch("KEY", "Payments")` keeps matching the same branch. New filters can use either name.
- **Delete:** if you delete a component, a filter that names it keeps matching the components that used to sit under it, so boards keep loading.

## Errors

- A name that has never existed in the space gives an error, such as *Component "Nope" not found in project KEY*. This matches how Jira's own `component = "Nope"` behaves.
- An unknown space key gives an error too.
