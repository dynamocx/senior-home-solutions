# Senior Home Solutions: Production Site

Agency: Dynamo CX (dynamocx.io). Client: **Senior Home Solutions** (seniorhomesolutions.com).

This is a **live production site with real traffic and rankings**, not a new build. The work is adding and improving pages. We build in WordPress/Elementor through the `shs-elementor` MCP server (see `.mcp.json` and README.md). This repo holds shared knowledge and coordination, not site code.

Shared Elementor/REST lessons (read these first):
@~/projects/_shared/elementor-playbook.md

## Site

| | URL |
|---|---|
| Production | https://seniorhomesolutions.com |

- Stack (seen in the public REST namespaces on 2026-09-30): WP Engine, Elementor + Elementor Pro, ElementsKit, JetEngine (+ Jet Reviews, Jet Search, Jet Smart Filters), UAEL (Ultimate Addons), ACF, CPT UI, Yoast, WP Rocket, Trustindex, Google Site Kit, CallTrk, OptinMonster, If-So, Code Snippets, WP All Import, Elementor MCP Composer 1.0.17, Angie, The Plus Addons (`tp-heading-title` widgets on service pages). **Forms are Elementor Pro forms connected to GHL/LeadConnector (msgsndr), not Gravity Forms.** Don't touch them.
- Hello Elementor theme. Kit post ID **10** (`.elementor-kit-10`). Site-wide Header template **36**, Footer template **42**.
- Main menu: Wheelchair Ramp Rental · Wheelchair Ramp Installation · Service Area (`/locations`) · Products for Sale (Catalog, Ramps, Stair Lifts, Grab Bars, Accessories, Tub to Shower) · Services (ADA Construction overview, Bathroom, Kitchen, Accessibility Renovation, Mobility Consulting) · Our Company (About, Our Work, Reviews, FAQ, Contact, Locations, Blog) · Get a Quote (→ `/contact-us/`).

### Content types (public REST, 2026-09-30)

| Type | URL pattern | Count | Single template |
|---|---|---|---|
| Pages | `/slug/`, services under `/ada-construction-services/…` | 19 | none (per page) |
| `service-area` | `/locations/michigan/[city]/`, state page `/locations/michigan/` (ID 446) | 61 | city pages render single template **638** |
| `case-study` | `/our-work/[slug]/` | 14 | **461** |
| `products` | `/products/[slug]/` | 8 | **658** |
| Posts | `/[slug]/` (blog index `/blog/`, page 477) | 18 | **453** |

### Theme Builder templates (MCP `list-site-parts`, 2026-09-30)

| ID | Type | Title | Conditions |
|---|---|---|---|
| 36 / 42 | header / footer | Header 01 / Footer 01 | site-wide (live) |
| 37 / 43 | header / footer | Header 02 / Footer 02 | page 105 only (page not public) |
| 638 | single | Single Service Area Template | all `service-area` |
| 832 | single | Office Location | service-area 269, 498 (Grand Rapids), 499 (Sterling Heights) |
| 830, 1212 | single | Service Area Template / Backup-Location Template | unassigned |
| 461 | single | case-study single | all `case-study` |
| 658 | single | products single | all `products` |
| 453 | single | Single Post | all posts |
| 452 / 456 / 553 / 693 | archive | blog / case-study / service-area / products archives | their post-type archives |
| 898 | archive | product category | `product-category/24` (Wheelchair Ramps) |
| 1118 | search-results | | search |
| 202 | section | sticky-footer-mobile | none (inserted by shortcode or template) |
| 471, 1222 (+455, 460 drafts) | loop-item / single | loop items | none |

## Production rules (stricter than a new build)

- **Schema (JSON-LD) goes in Elementor → Custom Code** (`elementor_snippet` posts), with display conditions targeting the relevant pages. Never add it as an HTML widget on a page. Changing it counts as an SEO change, so it needs Bret's go-ahead.

- Build new pages as **drafts** only. Never publish, and never change menus, kit settings, global classes, templates, caching, redirects, or Yoast/SEO settings, without Bret's go-ahead.
- **Back up before every template or REST write** (`backups/`, dated filename, commit it).
- **Add new global classes only; never edit or reorder existing ones** (they style live pages).
- **Protect rankings:** don't change slugs or delete pages without a 301 redirect in place; don't remove indexed content without asking.
- Don't touch tracking snippets (GA, Meta Pixel, GHL) or form integrations (Elementor forms → GHL) unless asked.
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
- **V3 vs V4:** the whole site is **V3**. Every page sampled (home, contact, about, services, ramp rental, a city page, a case study, a product) uses V3 containers and widgets (Elementor, ElementsKit, The Plus, UAEL), with no V4 atomic elements.
- **Global classes: none** (`elementor://global-classes` is empty as of 2026-09-30).
- **This limits what the MCP can do.** It can only create or edit **V4** elements. It can read V3 pages but can't change them. That leaves three options:
  1. Build new pages in **V4 through the MCP**, with a new set of global classes that recreates the V3 look (kit colors and fonts, 1.2× type scale). It's fast, and the classes can be reused, but these would be the site's first V4 pages, so they may not match the existing ones pixel for pixel.
  2. **Duplicate a V3 page** in WP admin, then change the copy in the editor or through REST `_elementor_data` (the playbook's V3 REST section). This matches the existing pages exactly, but every edit goes through JSON, which is slower and more fragile.
  3. Mix them: V4 body sections inside the existing V3 header and footer (which happens automatically), and copy the V3 Bottom CTA pattern.
  **Decision (Bret, 2026-09-30): option 1, build new pages in V4 through the MCP.** Create a new set of global classes that matches the kit, and document them here.
- **Reference page: Wheelchair Ramp Rental (229).** Its section flow is the standard pattern for service pages: Page Title (Lottie + `tp-heading-title`) → Intro Block (icon-box + text) → reviews shortcode → Priority Well (text, icon lists, HTML) → "More Quality" 4-card image/icon-box grid → 3 image-boxes → Portfolio (Our Work) → Call to Action → FAQ (`uael-faq` with schema) → Bottom CTA (ElementsKit heading + button). ADA Construction Services (226) follows the same frame, with a Services card grid, Features, Team and Blog sections. There is no class map because the site is V3.

## Known issues (found 2026-09-30, not fixed)

- ~~Wrong business schema on `/locations/michigan/` (service-area 446)~~ **Fixed 2026-09-30 by Bret:** Bret deleted the Delong Plumbing JSON-LD widget `7ae02e23` in the editor. A backup of the page before the fix is in `backups/`. The empty "Schema" container `be6429d` is still on the page.
- The site tagline is still the WP Engine default "Your SUPER-powered WP Engine Site", and it appears in the WebSite schema. Changing it is a Yoast/settings change, so it needs Bret's approval.
- The menu's `/product-category/wheel-chair-ramps/` link resolves (200), but its taxonomy isn't exposed in REST. It's probably a JetEngine or CPT UI taxonomy, so check it before building product pages.

- **Grand Rapids case study (407) shows unfilled template text on the live site** (the JetEngine "Challenge" field on the post itself, rendered by widget `eb8dfc2` in template 461; other case studies are fine) ("Context: Why did the family reach out? (e.g., …Toledo…)"). Its details ("same day as discharge" vs "48 hour turnaround") also conflict. It needs real copy.

## Landing pages (PPC)

- Build on **Elementor Canvas** (`template: elementor_canvas`) so the global header and footer, and their CallRail-swapped main number, don't appear. GA4, GTM, Meta Pixel, Google Ads and CallRail `swap.js` still load on Canvas. CallRail left the 616 tracking number unchanged in testing (2026-09-30).
- **GHL form embed:** the Master-Lead-Gen iframe (`link.dynamocx.com/widget/form/GA5m1RhSONQyjwU0zUg5` + `form_embed.js`) lives in a V3 HTML widget on Contact (489, widget `f07b773`). V4 has no HTML element, so add an HTML widget to the page's `_elementor_data` via REST (back up first), then make any MCP edit so the preview snapshot picks it up. MCP preview links render the latest *revision*, and REST meta writes don't create one.
- Use local styles on the page, not new global classes, so the page is self-contained.

## First-session checklist

1. Confirm the MCP works (`core-get-site-info`). If every tool fails, check Angie consent at `wp-admin/admin.php?page=angie-app`.
2. Inventory: kit, global classes, templates and their display conditions, CPTs, main menu.
3. Fill in **Business facts** and **Design system** above; create PAGES.md rows for the pages in scope.

Status: **done 2026-09-30.** The MCP works as Bret's user. Items still open: Bret's V3/V4 build decision, the (?) business facts, and the Known issues below.

**MCP auth on macOS:** the desktop app doesn't read `~/.zshrc`. Run `launchctl setenv SHS_WP_AUTH "$SHS_WP_AUTH"` in Terminal.app, then quit Claude with Cmd+Q and reopen it. This resets on reboot.
