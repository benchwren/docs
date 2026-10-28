---
title: Privacy policy
nav_order: 4
permalink: /legal/privacy/
---

# Privacy policy

**Effective date:** 28 October 2026

Benchwren is the trading name of Shray Kumar, a sole proprietor based in India, who is the Atlassian Marketplace partner for our apps.

This policy explains what personal data Benchwren handles, why, and what you can do about it. It covers:

- Benchwren apps: **Component Tree for Jira** and **Sprint Scope for Jira**;
- the websites `benchwren.com` and `docs.benchwren.com`;
- email support at `support@benchwren.com`.

Benchwren is the trading name of Shray Kumar, an individual based in Gurugram, Haryana, India ("Benchwren", "we", "us"). For anything in this policy, contact **support@benchwren.com**.

## The short version

- Our apps run entirely on the platform they extend. Component Tree for Jira and Sprint Scope for Jira run on Atlassian's cloud (Atlassian Forge). Benchwren has no servers, and your Jira content never comes to us.
- We don't sell personal data, show ads or use tracking cookies.
- We see a small amount of information: the contact details Atlassian shares with app vendors, app error logs, and whatever you send us in support emails.

## Component Tree for Jira

### What the app stores, and where

The app keeps everything inside your Atlassian cloud site, on infrastructure run by Atlassian:

| Data | Where it lives |
|---|---|
| The component tree: which component sits under which, and in what order | Forge storage for your site, run by Atlassian |
| A snapshot of component names, and the former names of renamed or deleted components, so saved filters keep working | Forge storage for your site |
| The "Component path" value on each work item | A field in your Jira site |

The app reads spaces (projects), components and work items in your site to do its job. It doesn't store work item content, comments, attachments or information about users. Before it reads or changes anything, it checks the permissions of the person using it, as that person. It counts work items as that person too. Background updates run as the app.

Component names and paths are your organisation's data. They may contain personal data if, for example, someone names a component after a person. If so, that data stays in your Jira site under your organisation's control.

### What we can see

- **App logs.** When the app runs, it writes short technical log messages: internal IDs (such as space and component ID numbers), counts, and error messages from Jira when something fails. Atlassian makes these logs available to us in its developer console unless a site admin turns off log sharing for the app. We use them only to find and fix problems. Atlassian keeps them for a limited period that it sets.
- **Licence and contact details from Atlassian.** When an organisation installs, evaluates or buys the app, Atlassian shares licence information with us through its Marketplace reports. This can include the organisation's name and site address and the names and email addresses of its technical and billing contacts. We use it to manage licences, provide support and send important notices about the app. We don't use it for unrelated marketing.
- **Usage metrics from Atlassian.** Atlassian gives app vendors aggregate statistics, such as install counts and invocation counts. These don't identify individual users.

We can't see your Jira content, and we don't receive it.

### When you uninstall

Uninstalling the app removes its access to your site. Atlassian deletes the app's Forge storage for your site under its retention rules for Forge apps. Values already written to the Component path field stay in your Jira site until you remove them.

## Sprint Scope for Jira

### What the app stores, and where

The app keeps everything inside your Atlassian cloud site, on infrastructure run by Atlassian:

| Data | Where it lives |
|---|---|
| For each sprint the app's functions have been used on: the ids and creation dates of the work items that were in it, and when it was last checked | Forge storage for your site, run by Atlassian |
| Saved function results (lists of work item ids) | Your Jira site, which stores the results of JQL functions |

The app only reads Jira; it never changes work items, sprints or boards. It reads sprints, boards, work items and the history of the Sprint field. It doesn't store work item content, comments, attachments or information about users. It reads as the app, and Jira applies each person's own permissions to the results, so nobody sees a work item they couldn't already see.

### What we can see

The same as for Component Tree for Jira: app logs, licence and contact details from Atlassian, and aggregate usage metrics. Sprint Scope's logs also include the sprint name or id that someone typed into one of its functions.

### When you uninstall

Uninstalling the app removes its access to your site. Atlassian deletes the app's Forge storage for your site under its retention rules for Forge apps. Your sprints and work items are not changed.

## Support

When you email `support@benchwren.com`, we receive your name, email address and whatever you include in the message, such as screenshots or details about your site. We use this only to answer you and to improve the app. Please don't send passwords, API tokens or other secrets.

We keep support emails for up to 24 months after our last exchange, unless we need them longer to handle a legal claim.

## Our websites

`benchwren.com` and `docs.benchwren.com` are static sites hosted by GitHub (GitHub Pages).

- They set no cookies and run no analytics or tracking scripts.
- Fonts and other files are served from our own domain, so your browser doesn't contact other companies when you visit.
- Like any web host, GitHub processes your IP address and browser details to deliver the pages and protect its service. GitHub's own privacy statement covers that processing.

## Who processes data for us

| Provider | What it does for us |
|---|---|
| Atlassian | Hosts and runs the app (Forge); runs the Marketplace, licensing and payments; provides app logs and reports |
| GitHub | Hosts our websites |
| Cloudflare | Runs our domain's DNS and forwards email sent to `support@benchwren.com` |
| Google (Gmail) | Stores and delivers our support email |

These providers may process data outside India, including in the United States. Each one handles data under its own terms and privacy policy.

## Why we're allowed to use this data

- **To provide the app and support** (logs, licence details, support emails): to perform our agreement with you or your organisation.
- **To keep the app working and secure, and to send important notices about it:** our legitimate interest in running a reliable product.
- **To meet legal obligations:** where the law requires us to keep or disclose information.

## How long we keep it

| Data | Kept for |
|---|---|
| App logs | The period Atlassian sets; we don't copy them elsewhere except to investigate a specific problem |
| Licence and contact details | While the licence is active, plus up to 24 months |
| Support emails | Up to 24 months after our last exchange |

## Your rights

Depending on where you live, including under India's Digital Personal Data Protection Act 2023 and the EU and UK GDPR, you can ask us to:

- tell you what personal data we hold about you and give you a copy;
- correct it or bring it up to date;
- delete it;
- stop or limit how we use it, or object to a use;
- withdraw consent, where we rely on consent.

Email **support@benchwren.com**. We'll reply within 30 days. If you're not satisfied with our answer, you can complain to your local data protection authority. In India, that's the Data Protection Board of India.

Data inside your Jira site, such as component names and Component path values, is controlled by your organisation. For that data, contact your Jira site admin.

## Security

Our apps follow Atlassian's Forge security model:

- They ask only for the permissions they need.
- Their data is stored by Atlassian for your site alone.
- In Component Tree for Jira, every change to the tree is checked on Atlassian's servers before it's saved. Sprint Scope for Jira only reads your site.

Each app's Data and security page lists its permissions and known limits: [Component Tree](https://docs.benchwren.com/atlassian/component-tree/data-and-security/), [Sprint Scope](https://docs.benchwren.com/atlassian/sprint-scope/data-and-security/).

## Children

Our apps and websites are for businesses. They aren't meant for children, and we don't knowingly collect children's data.

## Changes to this policy

If we change this policy, we'll update the effective date above. For significant changes, we'll also tell licence contacts by email before the change takes effect.

## Contact

Shray Kumar, trading as Benchwren
Gurugram, Haryana, India
**support@benchwren.com**
