# docs.benchwren.com

Public docs for Benchwren apps.

- Built by GitHub Pages with Jekyll and the [Just the Docs](https://just-the-docs.com/) theme (`remote_theme` in `_config.yml`). There's no build step here: push to `main` and Pages rebuilds.
- Served at `https://docs.benchwren.com` (see `CNAME`). DNS is at Cloudflare and must stay **DNS only** (grey cloud) so GitHub can issue the HTTPS certificate.
- Apps are grouped by platform: one folder per platform (`atlassian/`), one folder per app inside it (`atlassian/component-tree/`). A platform's `index.md` has `has_children: true`; an app's `index.md` has `parent: <Platform>` and `has_children: true`; app pages have `parent: <App title>` and `grand_parent: <Platform>`.
- To add a platform later (for example Slack), copy `atlassian/index.md` to `slack/index.md`, change the title and permalink, and add it to the home page.
