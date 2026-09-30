# Senior Home Solutions: Production Site

Agency: Dynamo CX (dynamocx.io). Client: **Senior Home Solutions** (seniorhomesolutions.com).

This is a **live production site with real traffic and rankings**, not a new build. The work is adding and improving pages. We build in WordPress/Elementor through the `shs-elementor` MCP server (see `.mcp.json` and README.md). This repo holds shared knowledge and coordination, not site code.

Shared Elementor/REST lessons (read these first):
@~/projects/_shared/elementor-playbook.md

## Site

| | URL |
|---|---|
| Production | https://seniorhomesolutions.com |

- Stack (seen in the public REST namespaces on 2026-09-30): WP Engine, Elementor + Elementor Pro, ElementsKit, JetEngine (+ Jet Reviews, Jet Search, Jet Smart Filters), UAEL (Ultimate Addons), ACF, CPT UI, Yoast, WP Rocket, Trustindex, Google Site Kit, CallTrk, OptinMonster, If-So, Code Snippets, WP All Import, Elementor MCP Composer 1.0.17, Angie. **Not seen:** a Gravity Forms REST namespace or The Plus Addons, so confirm which form plugin feeds GHL before touching any form.
- Hello Elementor theme. Kit post ID **10** (`.elementor-kit-10`). Site-wide Header template **36**, Footer template **42**.
- Main menu: Wheelchair Ramp Rental · Wheelchair Ramp Installation · Service Area (`/locations`) · Products for Sale (Catalog, Ramps, Stair Lifts, Grab Bars, Accessories, Tub to Shower) · Services (ADA Construction overview, Bathroom, Kitchen, Accessibility Renovation, Mobility Consulting) · Our Company (About, Our Work, Reviews, FAQ, Contact, Locations, Blog) · Get a Quote (→ `/contact-us/`).

### Content types (public REST, 2026-09-30)

| Type | URL pattern | Count | Single template |
|---|---|---|---|
| Pages | `/slug/`, services under `/ada-construction-services/…` | 19 | none (per page) |
| `service-area` | `/locations/michigan/[city]/`, state page `/locations/michigan/` (ID 446) | 61 | city pages render single template **638** |
| `case-study` | `/our-work/[slug]/` | 14 | **461** |
| `products` | `/products/[slug]/` | 8 | **658** |
| Posts | `/[slug]/` (blog index `/blog/`, page 477) | 18 | not checked |

Template IDs come from `data-elementor-id` on the rendered pages. Display conditions still need checking through the MCP.

## Production rules (stricter than a new build)

- Build new pages as **drafts** only. Never publish, and never change menus, kit settings, global classes, templates, caching, redirects, or Yoast/SEO settings, without Bret's go-ahead.
- **Back up before every template or REST write** (`backups/`, dated filename, commit it).
- **Add new global classes only; never edit or reorder existing ones** (they style live pages).
- **Protect rankings:** don't change slugs or delete pages without a 301 redirect in place; don't remove indexed content without asking.
- Don't touch tracking snippets (GA, Meta Pixel, GHL) or form integrations (Gravity Forms → GHL) unless asked.
- Check PAGES.md and claim a page before touching it.

## Business facts

Taken from the live site on 2026-09-30. **Bret still needs to confirm the items marked (?).**

- **Name:** Senior Home Solutions (legal: Senior Home Solutions of Michigan Inc., per the About page)
- **Address:** 11471 Orchardview Dr, Fenton, MI 48430 (Contact page)
- **Phone:** (586) 999-9042 (`tel:+15869999042`). Note that the site links it in three different `tel:` formats.
- **Services:** wheelchair ramp rental, sales and installation (modular aluminum, portable, threshold ramps; used ramps too); stair lifts; grab bars; tub-to-shower conversions; ADA bathroom and kitchen remodels; accessibility renovation; mobility consulting. Residential and commercial work. There is also a referral audience page for medical and insurance professionals (case managers, discharge planners, care facilities).
- **Service area:** Michigan. The contact-page area picker lists Flint/Mid-Michigan, Lansing, Detroit Metro, Ann Arbor, Grand Rapids/West Michigan, Kalamazoo/Southwest, and Traverse City/Northern Michigan. There are 60 city pages.
- **Claims already on the site:** "serving for over 20 years", "Family Owned", "Locally Owned", "48 hour turn around" (the footer qualifies this as "strive to maintain 48 hours or less… for most ramps and grab bars within our greater metro service areas"), a Certified Aging in Place Specialist on staff, an industry lifetime warranty on aluminum ramp *purchases*, a 5.0 rating from roughly 240–250 Google reviews via Trustindex, and a response to all inquiries within 24 hours.
- **Tone:** warm, reassuring and practical, and speed is the main selling point ("Rapid Response"). Speaks to families and caregivers as well as seniors.
- **Team:** (?) There is an About page `#team` section, but it hasn't been reviewed yet.
- **Never claim:** (?) Ask Bret. Until then, don't extend the lifetime warranty to rentals, don't promise 48 hours without the qualifier, and don't claim Medicare/insurance coverage.

## Design system

- **Kit colors (kit 10):** primary `#25293D` (navy), secondary `#3550A8` (blue), text `#777777`, accent `#FFFFFF`, plus customs `#F7F7F7` (light bg), `#1E1B1B`, `#FFD974` (yellow highlight), `#D2D2D2`, `#FFFFFF33`, `#131E4A36`.
- **Kit fonts:** headings **Sora** 700; body **Manrope** 500 16px/1.8. Custom heading scale is roughly 1.2×: 47.78 / 39.81 / 33.18 / 27.65 / 23.04 / 19.2px.
- **V3 vs V4:** every page sampled (home, contact, about, services, ramp rental, a city page, a case study, a product) is **V3 containers with no atomic V4 elements**. Build new pages in V3 to match.
- **Global classes:** none appear in the rendered HTML, which fits a V3 site. Still to confirm via `elementor://global-classes` once the MCP connects.
- **Reference page:** (?) not chosen yet. Possible candidates are Wheelchair Ramp Rental (229) and ADA Construction Services (226), which are the most-built service pages. Pick one after reading their element trees through the MCP.

## Known issues (found 2026-09-30, not fixed)

- **Wrong business schema on `/locations/michigan/` (service-area 446):** HTML widget `7ae02e23` outputs JSON-LD for **"Delong Plumbing Lake Orion"** (a Plumber with a delongplumbingmi.com URL and a 248 phone number). It was probably pasted from another client, and it sends Google conflicting business data. The fix needs Bret's approval.
- The site tagline is still the WP Engine default "Your SUPER-powered WP Engine Site", and it appears in the WebSite schema. Changing it is a Yoast/settings change, so it needs Bret's approval.
- The menu's `/product-category/wheel-chair-ramps/` link resolves (200), but its taxonomy isn't exposed in REST. It's probably a JetEngine or CPT UI taxonomy, so check it before building product pages.

## First-session checklist

1. Confirm the MCP works (`core-get-site-info`). If every tool fails, check Angie consent at `wp-admin/admin.php?page=angie-app`.
2. Inventory: kit, global classes, templates and their display conditions, CPTs, main menu.
3. Fill in **Business facts** and **Design system** above; create PAGES.md rows for the pages in scope.

Status 2026-09-30: step 3 was done from the public site. Steps 1–2 are still open because the MCP returned 401: `SHS_WP_AUTH` wasn't in the app's environment. Still to do via the MCP: global classes, template display conditions, and choosing the reference page.
