# Voice, trademarks and naming

## Who Gerber is, in its own words

- Founded in **1928**. The Gerber Baby trademark dates from 1931, and the Onesies® Brand bodysuit was invented in **1982**.
- Mission: to "nurture, support, and bring smiles to families and their little ones worldwide."
- Values named on the site: "care and commitment" and "excellence."
- Current taglines: "More wear in every wear™" and "Anything For Baby™". For Onesies®: "The Most Recognizable Name in Baby Clothes™".

Quote taglines exactly, with their marks, or not at all. Don't invent new taglines in Gerber's name.

## Tone

**Customer-facing copy:** warm, reassuring and practical, like a friend who has raised a few kids. Write short sentences and lead with the benefit to the parent and the comfort of the baby. Seasonal fun is welcome (the site uses headings like "Pumpkin Patch Picks"), but keep it light and never sarcastic.

**Internal tools** (warehouse, ops, admin): keep the warmth but put clarity first. Say what's wrong, then exactly what to do. Use the system's real terms where staff use them, such as SAP, Deposco, wave, IDoc and EA/PK, and explain anything a picker wouldn't know. No exclamation marks in error or status messages.

| Do | Don't |
|---|---|
| "This order can't ship yet. Here's how to fix it." | "Oops! Something went wrong 😬" |
| "Soft, breathable cotton for sensitive skin." | "Revolutionary next-gen fabric technology." |
| "Sizes newborn to 5T." | "Sizes for all your little guys and gals." |

## Trademark rules

Gerber actively protects these marks, and in particular stops "Onesies" from becoming a generic word.

- **Onesies®** is a brand, not a noun. Write "Onesies® Brand bodysuits" or "Onesies® Brand short-sleeve bodysuits". Never write "a onesie", "onesies" (lowercase) or "Onesies" without ®. When the item isn't specifically Onesies® Brand, call it a **bodysuit**.
- **Gerber®**: use the ® on the first prominent mention on a page or screen, then plain "Gerber".
- Other marks seen on the site include modern moments™ by Gerber® and Grow-With-Us Perks®. Partner and licensed marks appear as in "HARRY POTTER™ x Gerber®". Keep the licensor's mark and its capitalization exactly.
- Superscript marks with the `.gcw-tm` class from `tokens.css`.
- Internal prototypes still follow these rules. Screenshots travel.

## Product naming pattern

Product titles on the site follow a consistent order:

`[Pack or piece count] [Age group] [Gender] [Theme or print] [Product type]`

- "3-Pack Baby Neutral Pumpkins Active Pants"
- "2-Piece Infant & Toddler Neutral Halloween Ghosts Cotton Pajamas"
- "Baby Girls Hogwarts Varsity Stripe Dress"
- "8-Pack Baby Neutral Holiday Drooling Bibs"

The parts:
- **Count:** "3-Pack", "8-Pack", "2-Piece".
- **Age group:** Baby, Infant, Toddler, or "Baby & Toddler" / "Infant & Toddler".
- **Gender:** Boys, Girls, Neutral.
- **Product type:** Bodysuit, Sleep 'N Play, Romper, Footless Pajamas, Bibs, and so on. "Sleep 'N Play" is written with an apostrophe-N.

Use this pattern for mock product data in prototypes too. For example, "5-Pack Baby Neutral Assorted Short-Sleeve Bodysuits" reads as Gerber, while "Bodysuit 5pk asst" doesn't. In dense tables, show the SKU or code next to the name and keep the full name in its own column or a tooltip.

## Sizes and ages

These are size values as they appear in the site's product data (60 products sampled on 2026-10-01). Use them exactly, with a plain hyphen and no spaces:

- **Baby:** `NEWBORN`, `0-3M`, `3-6M`, `6-9M`, `12M`, `18M`, `24M`
- **Toddler:** `2T`, `3T`, `4T`, `5T`
- **Kids:** `6`, `6/7`, `7`, `8`, `10`, `10/12`
- **Shoes:** `6C`, `7C`, `8C`, `10C`, `12C`

In running copy, spell sizes out for parents ("sizes newborn to 5T", "0-3 months"). In tables and pick screens, use the codes above.
