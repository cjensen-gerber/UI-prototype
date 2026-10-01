---
name: gerber-style-guide
description: Gerber Childrenswear visual and writing style guide (colors, Montserrat type, buttons, voice, trademark rules, product naming) with ready-to-use CSS tokens. Use whenever you create or update anything Gerber-branded or Gerber-internal in this repo, such as the Warehouse Order Assistant prototype, new UI screens, HTML artifacts, slides, docs or mockups, and whenever copy mentions Gerber products or trademarks (Onesies® Brand, Gerber®).
---

# Gerber Childrenswear style guide

This skill describes how Gerber Childrenswear looks and sounds in public. Use it for customer-facing mockups and for internal tools such as the warehouse prototype. It was built from Gerber's public website. **It is not Gerber's official brand book.** When Gerber's marketing team provides official guidelines, those win (see "Keeping this current").

## Precedence

1. What the user or the Gerber team asks for in the moment.
2. Official Gerber brand guidelines, once they're added to `references/`.
3. This skill.
4. General design defaults.

## How to use it

1. Link `tokens.css` or copy it into the page, and style through its variables. Don't hard-code hex values.
2. Read the reference that matches the job:
   - `references/brand.md`: the palette with named color schemes, typography, buttons and forms, imagery, the logo. Read it for any visual work.
   - `references/voice.md`: tone, trademark rules and product naming. Read it for any copy.
   - `references/internal-tools.md`: how to adapt the consumer brand for dense operational tools (warehouse, ops and admin screens). It covers status colors, data typography and dark mode. Read it for the prototype and any similar tool.
3. Before you finish, run the checklist below.

## The rules that matter most

- **Navy is the brand.** Text, primary buttons and key UI use Gerber Navy `#002744`. The page ground is warm Cream `#F9F5F3` or white, never grey.
- **Pastels are surfaces, not text.** Jordy blue, Maize, Geraldine coral, Seanymph sage and Sandy Brown each have a light tint. Use them for backgrounds, cards, chips and buttons, always with navy text on top. Never set body text in a pastel on a light background.
- **One typeface: Montserrat.** It comes from Google Fonts. Headings are weight 400 (Gerber headings are light, not bold). Eyebrows and subheadings are uppercase 600 with 0.05em tracking. Body text is 400 at about 1.575 line height.
- **Buttons are square and uppercase.** They have 0 radius, Montserrat 600, 0.02em tracking and a 44px height. Primary is navy with cream text. Secondary is a pastel with navy text, or a 1px navy outline.
- **Radius is 0 by default.** Gerber's retail UI is square-cornered. Small radii (4–8px) are acceptable only inside internal tools, for chips and inputs (see `internal-tools.md`).
- **Write warm, plain and parent-friendly.** Short sentences and no jargon in customer copy. Internal tools stay friendly but direct.
- **Use trademarks correctly.** Write "Onesies® Brand bodysuits". Never "onesie" or "onesies" as a generic noun, and never "Onesies" without ®. Write Gerber® on first prominent use. When there's no trademarked product, say "bodysuit".
- **Never redraw the logo or the Gerber Baby.** Use official files only (see `brand.md`). In prototypes, a text wordmark or no logo is fine.

## Checklist before you ship

- [ ] Every color comes from a `tokens.css` variable. Text on any surface is navy, cream or a token rated ≥ 4.5:1.
- [ ] Montserrat is loaded with a fallback stack, and headings are 400 weight, not bold.
- [ ] Buttons are square, uppercase and 600 weight. Only one primary (navy) button per view.
- [ ] Copy follows `voice.md`: no generic "onesie", trademarks marked, sizes and age ranges written Gerber's way.
- [ ] There is no recreated logo, no Gerber Baby artwork and no stock imagery passed off as Gerber photography.
- [ ] Status colors (internal tools only) come from the status tokens and always pair color with a word or icon.
- [ ] Mock data is labelled as mock, and real customer or order data never appears in shared prototypes.

## Keeping this current

- **Sources:** the public site https://www.gerberchildrenswear.com (Shopify theme tokens, read 2026-10-01) and its About Us page. See the "Sources" section in `references/brand.md`.
- The site's theme changes with seasonal campaigns. Re-check the palette at least once a quarter, or when the site is redesigned.
- When Gerber shares official brand guidelines, logo files or photography rules, save them under `references/official/` and update this file. Mark anything that the official material overrides.
