# Senior Home Solutions: Production Site

Agency: Dynamo CX (dynamocx.io). Client: **Senior Home Solutions** (seniorhomesolutions.com).

This is a **live production site with real traffic and rankings**, not a new build. The work is adding and improving pages. We build in WordPress/Elementor through the `shs-elementor` MCP server (see `.mcp.json` and README.md). This repo holds shared knowledge and coordination, not site code.

Shared Elementor/REST lessons (read these first):
@~/projects/_shared/elementor-playbook.md

## Site

| | URL |
|---|---|
| Production | https://seniorhomesolutions.com |

- Stack (same family as the Window Depot clone, verify on first session): WP Engine, Elementor Pro, ElementsKit, JetEngine, ACF, The Plus Addons, Yoast, WP Rocket, Gravity Forms, Trustindex reviews.
- Windowdepotpro.com was cloned from this site, so its architecture notes (the `service-area` CPT at `/locations/michigan/[city]/`, the City/Office/State location templates, and the `case-study`/`products` CPTs) probably match here. **Post and template IDs on production may differ, so verify before using any ID.**

## Production rules (stricter than a new build)

- Build new pages as **drafts** only. Never publish, and never change menus, kit settings, global classes, templates, caching, redirects, or Yoast/SEO settings, without Bret's go-ahead.
- **Back up before every template or REST write** (`backups/`, dated filename, commit it).
- **Add new global classes only; never edit or reorder existing ones** (they style live pages).
- **Protect rankings:** don't change slugs or delete pages without a 301 redirect in place; don't remove indexed content without asking.
- Don't touch tracking snippets (GA, Meta Pixel, GHL) or form integrations (Gravity Forms → GHL) unless asked.
- Check PAGES.md and claim a page before touching it.

## Business facts

TODO (fill in on the first session from the live site and Bret): services, NAP (name, address, phone), service area, certifications, team, tone of voice, and anything that must never be claimed.

## Design system

TODO (first-session inventory): kit colors and fonts, existing global classes (`elementor://global-classes`), which pages are V3 vs V4, and the best-built page to use as the reference template for new pages. Record the reference page ID and its class map here.

## First-session checklist

1. Confirm the MCP works (`core-get-site-info`). If every tool fails, check Angie consent at `wp-admin/admin.php?page=angie-app`.
2. Inventory: kit, global classes, templates and their display conditions, CPTs, main menu.
3. Fill in **Business facts** and **Design system** above; create PAGES.md rows for the pages in scope.
