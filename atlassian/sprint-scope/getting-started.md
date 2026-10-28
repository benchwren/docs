---
title: Getting started
parent: Sprint Scope for Jira
grand_parent: Atlassian
nav_order: 1
---

# Getting started

There's no configuration. After a Jira admin installs the app, anyone who can search Jira can use the functions, on any sprint that has started.

## 1. Pick a sprint

You can name a sprint in two ways:

- **By its name**, exactly as the board shows it, such as `"Sprint 14"`. Upper and lower case don't matter.
- **By its id**, such as `37`. Open the board's **Reports**, choose **Sprint burndown** and select the sprint. The id is the number after `sprint=` in the page address.

Names are quicker to type. Ids are safer in saved filters, because they keep working if someone renames the sprint or another sprint gets the same name.

## 2. Run a search

Open work item search, switch to **JQL**, and enter:

```
issue in addedAfterSprintStart("Sprint 14")
```

You'll see everything that joined the sprint after it started. Swap in `inSprintAtStart` for the committed scope, or `removedAfterSprintStart` for what was taken out. See [JQL functions](../jql-functions/) for what each one counts.

Jira's **Basic** search mode can't show JQL functions. Use **JQL** mode for these queries.

## 3. Save it and reuse it

Choose **Save filter** to keep the search. You can then:

- build a board from the filter;
- show it on a dashboard with the **Filter results** gadget;
- share it with your team.

Saved results stay current on their own. When work moves in or out of the sprint, the filter catches up within about 10 seconds.

For more ready-made searches, see [Sprint review recipes](../recipes/).
