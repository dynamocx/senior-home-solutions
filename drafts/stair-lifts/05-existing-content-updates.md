# Updates to Existing Stair Lift Content (from the content audit, 2026-10-12)

These are **proposed edits to live, indexed pages**. Nothing here has been changed on the site. Each needs Bret's go-ahead, and a backup first.

**Decided by Bret, 2026-10-12:** the flagship is the new `/stair-lifts/straight-stair-lifts/` page. `/products/lifts/` stays as a lightweight product page in the catalog and gets a link to the new pages once they're published. The blog posts link in as hub-and-spoke content. **None of these edits should go live until the four new pages are published**, or the links will 404.

What each page looks like today was read from the live site on 2026-10-12.

---

## 1. `/products/lifts/` — "Stair Lifts" product page

**Today:** titled "Stair Lifts", but the body is about wheelchair and platform lifts ("vertical wheelchair lifts and inclined platform lifts"), with one line naming Bruno stair lifts and an H2 about Humancare overhead lifts. The meta description says "wheelchair lift installations". It has no price, no checklist and no internal links. It's a `products` entry rendered by template 658, so its layout is shared with the other seven product pages.

**Audit action:** make it the flagship straight stair lift page.

**Decision:** leave it as a product page. Once the new pages are live, add this block at the top.

  > **Looking for a stair lift for your home?**
  > Most Michigan staircases can take a straight stair lift, installed in days, with a rail that attaches to the stair treads and not your walls.
  > **[See straight stair lifts and pricing →](/stair-lifts/straight-stair-lifts/)**

- Optional, and a Yoast change that needs Bret's go-ahead: the meta description currently says "wheelchair lift installations".
  Suggested: `Stair lifts and wheelchair lifts for Michigan homes and businesses, professionally installed. See straight stair lift pricing or request a quote.`

---

## 2. `/straight-vs-curved-stairlifts-which-one-fits-your-staircase/` — comparison blog

**Today:** a strong 2,250-word post that already has a "Two Straight Stairlifts vs. One Curved Stairlift" section. Problems found:

1. **A second, unrelated article is pasted into the same post.** After the closing section there's a second H1, "Outdoor Stairlifts for Michigan Homes: Handling Snow, Ice, and Harsh Winters", followed by seven more H2s. The page has two H1s.
2. **No meta description.**
3. **No conversion path.** There's no form and no link to a stair lift product page or the contact page. All 12 internal links go to location pages.
4. **A hard-coded phone number, 586-980-0049,** which differs from the site's main number and won't be swapped by CallRail. `[CONFIRM: is this number current?]`

**Audit action:** position the two-lift solution and drive form conversions.

**Proposed:**
- Move the "Outdoor Stairlifts" article into its own post (new URL, for example `/outdoor-stairlifts-michigan/`), so each post has one H1 and one topic.
- Meta description: `Straight or curved stairlift? See the cost, install time and fit for each, plus how two straight lifts can save $3,000–$7,000 on stairs with a landing.`
- After the first paragraph of "What Is a Straight Stairlift?", add:

  > Think your stairs are straight? [Check the 3-point fit list and see straight stair lift pricing](/stair-lifts/straight-stair-lifts/).

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
> Learn more about [Michigan straight stair lift installation](/stair-lifts/straight-stair-lifts/), or see the option for [stairs with a landing](/stair-lifts/stairs-with-landings/).

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
> Many homes need both: a ramp to get in the door and a [straight stair lift](/stair-lifts/straight-stair-lifts/) to reach the bedroom. We look at the whole home in one free visit.

---

## 5. `/how-to-age-in-place-with-products-from-senior-home-solutions/` — product ecosystem post

**Today:** the page's SEO title is **"Handicapping Your Home"**. It has one link to `/products/lifts/` with the anchor "stair lifts". Three other links point to `/product-catalog/…` URLs that look like they belong to the old site. I couldn't confirm whether they still resolve, so they need checking.

**Audit action:** use the exact anchor "straight stair lifts".

**Proposed:**
- Change the anchor from "stair lifts" to "straight stair lifts", pointing to `/stair-lifts/straight-stair-lifts/`.
- Reword that sentence so the anchor reads naturally, for example: "…wheelchair ramps, **straight stair lifts**, grab bars and comfort-height toilets…"
- Check the three `/product-catalog/` links and repoint any that are broken.
- Suggest a new SEO title, since "Handicapping Your Home" is dated wording: `How to Age in Place: Home Mobility Products That Help`. `[CONFIRM with Bret: this is a Yoast change.]`

---

## 6. `/home-improvements-and-modifications-for-aging-in-place/` — broad overview

**Today:** 1,360 words with **no internal links**. It has four outbound links, including two to Redfin city pages ("condo in Dallas, TX", "home in Portland, OR"), so it reads as a syndicated article. It includes the sentence "Install a stairlift. This is a great alternative when walking up stairs becomes more difficult."

**Audit action:** add a high-visibility banner for a free in-home stair assessment.

**Proposed:**
- Link "Install a stairlift" to `/stair-lifts/straight-stair-lifts/`, with the anchor "Install a straight stair lift".
- Add this banner directly after that paragraph, and repeat it at the end of the post:

  > **Free In-Home Stair Assessment**
  > Worried about someone on the stairs? A Senior Home Solutions specialist will measure your staircase, check the whole home for fall risks, and give you a firm price. No cost and no obligation.
  > **[Book My Free Stair Assessment →](/contact-us/)** · or call `[PHONE]`

- Consider removing the two Redfin city links, which send readers to out-of-state real-estate listings.

---

## Order of work

1. Build and publish the four new pages.
2. Add the link block to `/products/lifts/`.
3. Make the five blog edits above (back up each post first).
4. Split the "Outdoor Stairlifts" article out of the comparison post.
