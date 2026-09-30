# Page Ownership

Claim a page here **before** editing it (commit and push the claim). Only one person edits a page at a time, because the Elementor MCP overwrites whole pages.

Status: `planned` · `claimed` · `draft built` · `in review` · `published`

## Shared / site-wide (one owner only)

| Area | Owner | Notes |
|---|---|---|
| Global classes, kit colors/fonts | Bret | Others add new classes only; live site |
| Header / footer / menus | Bret | |
| Caching, redirects, SEO settings | Bret | |

## Pages

| Page | URL | WP ID | Owner | Status | Notes |
|---|---|---|---|---|---|
| Grand Rapids PPC landing page | TBD (draft) | TBD | Claude (for Bret) | claimed | V4 on Elementor Canvas (no global header/footer); tracking number 616-681-4429; based on /locations/michigan/grand-rapids/ (498) |
| Homepage | `/` | 40 | — | published | |
| Wheelchair Ramp Rental | `/wheelchair-ramp-rental/` | 229 | — | published | Reference-page candidate |
| Wheelchair Ramp Installation | `/wheelchair-ramp-installation/` | 1122 | — | published | |
| ADA Construction Services | `/ada-construction-services/` | 226 | — | published | Reference-page candidate; parent of 4 service pages |
| ADA Bathroom Remodel | `/ada-construction-services/ada-bathroom-remodel/` | 989 | — | published | |
| ADA Kitchen Remodel | `/ada-construction-services/ada-kitchen-remodel/` | 1010 | — | published | |
| Accessibility Renovation | `/ada-construction-services/accessibility-renovation/` | 1022 | — | published | |
| Mobility Consulting | `/ada-construction-services/mobility-consulting/` | 1108 | — | published | |
| For Medical & Insurance Professionals | `/for-medical-insurance-professionals/` | 1568 | — | published | No `wp-page` Elementor doc rendered, so check how it's built |
| About | `/about-senior-home-solutions/` | 982 | — | published | |
| Reviews & Testimonials | `/testimonials/` | 97 | — | published | |
| FAQ | `/senior-home-solutions-faq/` | 484 | — | published | |
| Contact | `/contact-us/` | 489 | — | published | Form → GHL; don't touch |
| Blog | `/blog/` | 477 | — | published | |
| Giveaway | `/giveaway/` | 1315 | — | published | Campaign |
| Thank You / Thank You 250 | `/thank-you/`, `/thank-you-250/` | 1326, 1338 | — | published | Conversion pages; tracking |
| Landing Page Template | `/landing-page-template/` | 520 | — | published? | Publicly reachable; check whether it should be noindex |
| Privacy Policy | `/privacy-policy/` | 3 | — | published | |
| Michigan (state location) | `/locations/michigan/` | 446 (service-area) | — | published | Contains DeLong Plumbing schema; see CLAUDE.md Known issues |

CPT entries (60 city pages, 14 case studies, 8 products, 18 posts) are managed through their templates (see CLAUDE.md). Add a row here when you claim an individual entry.

## What to tell Claude about direct Elementor edits
- **No need to mention:** cosmetic changes (spacing, images, styling, copy polish). Claude re-reads the live version before writing.
- **Do mention (one line is enough):** template display conditions, element IDs being deleted or replaced, ACF fields or choices, slugs and URLs, new business facts.
- **Never edit the same document at the same time.** Save and close in Elementor before Claude writes, or reload before saving.
