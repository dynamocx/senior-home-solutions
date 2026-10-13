# Updates to Existing Stair Lift Content (from the content audit, 2026-10-12)

These are **proposed edits to live, indexed pages**. Nothing here has been changed on the site. Each needs Bret's go-ahead, and a backup first.

`[STRAIGHT]` below means the flagship straight stair lift URL. That is either `/products/lifts/` (the audit) or `/stair-lifts/straight-stair-lifts/` (the strategy brief). **This has to be decided before any link is added.** See "Decision needed" at the bottom.

What each page looks like today was read from the live site on 2026-10-12.

---

## 1. `/products/lifts/` — "Stair Lifts" product page

**Today:** titled "Stair Lifts", but the body is about wheelchair and platform lifts ("vertical wheelchair lifts and inclined platform lifts"), with one line naming Bruno stair lifts and an H2 about Humancare overhead lifts. The meta description says "wheelchair lift installations". It has no price, no checklist and no internal links. It's a `products` entry rendered by template 658, so its layout is shared with the other seven product pages.

**Audit action:** make it the flagship straight stair lift page.

**Proposed:**
- If this URL becomes the flagship: replace the body with the copy in [02-straight-stair-lifts.md](02-straight-stair-lifts.md), and move the wheelchair-lift, platform-lift and Humancare content to its own product entry so it isn't lost.
- If the flagship is the new `/stair-lifts/straight-stair-lifts/` page: keep this page as a short catalog entry and add this block at the top.

  > **Looking for a stair lift for your home?**
  > Most Michigan staircases can take a straight stair lift, installed in days, with a rail that attaches to the stair treads and not your walls.
  > **[See straight stair lifts and pricing →]([STRAIGHT])**

- New meta title: `Straight Stair Lifts for Michigan Homes | Senior Home Solutions`
- New meta description: `Affordable straight stair lifts, professionally installed in days. The rail mounts to your stairs, not your walls. Free home assessment across Michigan.`

---

## 2. `/straight-vs-curved-stairlifts-which-one-fits-your-staircase/` — comparison blog

**Today:** a strong 2,250-word post that already has a "Two Straight Stairlifts vs. One Curved Stairlift" section. Problems found:

1. **A second, unrelated article is pasted into the same post.** After the closing section there's a second H1, "Outdoor Stairlifts for Michigan Homes: Handling Snow, Ice, and Harsh Winters", followed by seven more H2s. The page has two H1s.
2. **No meta description.**
3. **No conversion path.** There's no form and no link to a stair lift product page or the contact page. All 12 internal links go to location pages.
4. **A hard-coded phone number, 586-980-0049,** which differs from the site's main number and won't be swapped by CallRail. `[CONFIRM: is this number current?]`
5. It says "Our installers check this during every site visit", which conflicts with the concierge and partner-installer positioning in the brief.

**Audit action:** position the two-lift solution and drive form conversions.

**Proposed:**
- Move the "Outdoor Stairlifts" article into its own post (new URL, for example `/outdoor-stairlifts-michigan/`), so each post has one H1 and one topic.
- Meta description: `Straight or curved stairlift? See the cost, install time and fit for each, plus how two straight lifts can save $3,000–$7,000 on stairs with a landing.`
- After the first paragraph of "What Is a Straight Stairlift?", add:

  > Think your stairs are straight? [Check the 3-point fit list and see straight stair lift pricing]([STRAIGHT]).

- Replace the last paragraph of the "Two Straight Stairlifts vs. One Curved Stairlift" section with:

  > **The money-saving option most families aren't told about.** If your staircase has a flat landing, ask for a two-lift quote before you agree to a custom curved lift. It can be installed in days, and it can save $3,000–$7,000.
  > **[See if your stairs qualify for the two-lift solution →](/stair-lifts/stairs-with-landings/)**

- In "Get a Free Stairlift Assessment in Michigan": add the GHL Master-Lead-Gen form (HTML widget) under the text, and replace the typed phone number with the site's standard phone link.

---

## 3. `/preparing-your-michigan-home-for-aging-in-place-home-modifications-a-room-by-room-guide/` — Michigan room-by-room guide

**Today:** 1,400 words with a "Hallways and Stairs" H2 and a one-line "Stairlifts" bullet. **The post has no internal links at all.**

**Audit action:** add an explicit "Stair Safety" section with a regional anchor.

**Proposed: add this H3 inside "Hallways and Stairs", after the Stairlifts bullet.**

> ### Stair Safety in Michigan's Multi-Level Homes
> Colonials, bi-levels and homes with basement laundry are everywhere in Michigan, and every one of them puts a staircase between you and a room you use daily. If the stairs are starting to feel risky, there are three steps to take, in order:
>
> 1. **Add a second handrail** and bright lighting at the top and bottom.
> 2. **Check the treads** for loose carpet and worn edges.
> 3. **Consider a stair lift.** Most Michigan staircases run in a straight line, which means a standard straight lift can be fitted in a few hours with a rail that attaches to the stair treads, not the walls.
>
> Learn more about [Michigan straight stair lift installation]([STRAIGHT]), or see the option for [stairs with a landing](/stair-lifts/stairs-with-landings/).

---

## 4. `/why-ada-compliant-ramps-matter-safety-and-accessibility-for-seniors/` — ADA ramp blog

**Today:** 1,190 words about ramps. Stair lifts aren't mentioned. Internal links: only the contact page.

**Audit action:** add an inline callout comparing ramps and stair lifts for entry stairs.

**Proposed: add this callout after "Platforms: More Than a Landing Pad".**

> **Ramp or stair lift? A quick guide for entry stairs**
>
> | | Wheelchair ramp | Stair lift |
> |---|---|---|
> | Best for | Wheelchair and scooter users | People who walk but struggle with steps |
> | Where | Outdoor entries with room for a gentle slope | Indoor stairs, and outdoor steps where a ramp won't fit |
> | Space needed | About 1 foot of ramp for every inch of rise | Fits on the existing stairs |
> | Short-term need | Can be rented | `[CONFIRM: are stair lift rentals offered?]` |
>
> Many homes need both: a ramp to get in the door and a [straight stair lift]([STRAIGHT]) to reach the bedroom. We look at the whole home in one free visit.

---

## 5. `/how-to-age-in-place-with-products-from-senior-home-solutions/` — product ecosystem post

**Today:** the page's SEO title is **"Handicapping Your Home"**. It has one link to `/products/lifts/` with the anchor "stair lifts". Three other links point to `/product-catalog/…` URLs that look like they belong to the old site. I couldn't confirm whether they still resolve, so they need checking.

**Audit action:** use the exact anchor "straight stair lifts".

**Proposed:**
- Change the anchor from "stair lifts" to "straight stair lifts", pointing to `[STRAIGHT]`.
- Reword that sentence so the anchor reads naturally, for example: "…wheelchair ramps, **straight stair lifts**, grab bars and comfort-height toilets…"
- Check the three `/product-catalog/` links and repoint any that are broken.
- Suggest a new SEO title, since "Handicapping Your Home" is dated wording: `How to Age in Place: Home Mobility Products That Help`. `[CONFIRM with Bret: this is a Yoast change.]`

---

## 6. `/home-improvements-and-modifications-for-aging-in-place/` — broad overview

**Today:** 1,360 words with **no internal links**. It has four outbound links, including two to Redfin city pages ("condo in Dallas, TX", "home in Portland, OR"), so it reads as a syndicated article. It includes the sentence "Install a stairlift. This is a great alternative when walking up stairs becomes more difficult."

**Audit action:** add a high-visibility banner for a free in-home stair assessment.

**Proposed:**
- Link "Install a stairlift" to `[STRAIGHT]`, with the anchor "Install a straight stair lift".
- Add this banner directly after that paragraph, and repeat it at the end of the post:

  > **Free In-Home Stair Assessment**
  > Worried about someone on the stairs? A Senior Home Solutions specialist will measure your staircase, check the whole home for fall risks, and give you a firm price. No cost and no obligation.
  > **[Book My Free Stair Assessment →](/contact-us/)** · or call `[PHONE]`

- Consider removing the two Redfin city links, which send readers to out-of-state real-estate listings.

---

## Decision needed: which URL is the flagship?

The two documents disagree.

| | Strategy brief | Content audit |
|---|---|---|
| Flagship straight lift page | new `/stair-lifts/straight-stair-lifts/` | existing `/products/lifts/` |
| Hub | new `/stair-lifts/` | not mentioned |

**Recommendation: follow the brief and build the new `/stair-lifts/` pages, then 301 `/products/lifts/` to `/stair-lifts/straight-stair-lifts/`.**

- `/products/lifts/` shares template 658 with seven other products, so it can't carry a fit checklist, pricing and an above-the-fold form without changing every product page or building a one-off template.
- Its slug says "lifts", not "stair lifts", and its content is mostly about wheelchair lifts, so there is little stair lift ranking to protect. The 301 passes on what there is.
- `/stair-lifts/` is currently unused (404), so the new structure is free to claim.
- The wheelchair-lift, platform-lift and Humancare content on that page needs a new home first (`/products/wheelchair-lifts/`, for example), or it disappears from the site.

A redirect and the menu change ("Stair Lifts" under Products for Sale) both need Bret's go-ahead.
