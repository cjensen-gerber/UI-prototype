# Applying the brand to internal tools

Gerber's public style is a retail storefront: airy, square and pastel. Internal tools such as the Warehouse Order Assistant are used under time pressure, often on a scanner or tablet in a bright warehouse. Keep them recognisably Gerber, and make these adjustments.

## What stays the same

- Navy ink on a cream or white ground, and Montserrat throughout.
- Uppercase, 600-weight buttons and eyebrows.
- Pastel tints as section and card grounds, with navy text.
- Voice rules and trademark rules (`voice.md`).

## What changes

| Retail site | Internal tool | Why |
|---|---|---|
| Radius 0 everywhere | Radius 0 on primary buttons. `--radius-tool` (6px) on chips, inputs and cards | Softer edges help users tell apart the many small controls in a dense layout |
| Body 14px | Body 15–16px, hit targets ≥ 44px | Read at arm's length on handhelds, with gloves |
| No status colors beyond badges | Status tokens: `--ok`, `--warn`, `--bad`, `--info` | People scan for state |
| Light only | Light by default, with optional dark mode via tokens | Night shifts and dim docks |
| Prices in 600 weight | Codes, IDs and quantities in `--font-mono` with tabular numbers | Order numbers, SKUs, IDoc numbers and bin locations must be easy to read and compare |

## Status colors

Each status has three tokens: text, soft fill and solid (for stripes and dots). All text pairs are ≥ 4.5 : 1 in both themes.

| Status | Use for | Light text / fill | Solid |
|---|---|---|---|
| `ok` | Resolved, matched, in sync | `#23705A` on Seanymph tint (5.1 : 1) | Seanymph |
| `warn` | Escalated, waiting on someone, ships today | `#8A5A00` on Maize tint (5.4 : 1) | Maize |
| `bad` | Mismatch, blocked, error | Sale red `#C4301C` on Geraldine tint (4.7 : 1) | Geraldine |
| `info` | In progress, selected, neutral highlight | Navy on Jordy tint (11.5 : 1) | Jordy |

Always pair a status color with a word ("Escalated") or a symbol (≠, ✓). Never rely on color alone.

The yellow "Prototype / mock data" banner should use the Maize solid with navy text (9.6 : 1). It's on-brand and still reads as a caution strip.

## Dark mode

Dark mode is defined in `tokens.css` and follows the OS setting unless `data-theme` is set on `<html>`. It uses a deep navy ground (`#0B1B2B`), cream text and Jordy as the accent. The pastels become the status text colors. Gerber's public site has no dark mode, so treat dark mode as a tool convenience, not a brand statement.

## Layout

- Put the summary before the detail. In the assistant, that's the diagnosis card first, then the steps.
- Show the two systems side by side, SAP then Deposco, always in that order, with mismatches marked.
- Put a person's next action in a numbered list only when it's a real sequence. Label each step with who does it.

## Applying it to the Warehouse Order Assistant (`index.html`)

The prototype predates this guide. To align it:
1. Swap its local palette for `tokens.css`. Its blue accent `#1D4F91` becomes `--gcw-navy`, its grey grounds become cream and white, and its hi-vis banner becomes Maize.
2. Replace IBM Plex Sans and IBM Plex Sans Condensed with Montserrat. Headings move to weight 400 and labels stay uppercase 600. Keep IBM Plex Mono for codes.
3. Square off the primary buttons (Send, New issue, Send escalation) and make them uppercase.
4. Rename mock items to the Gerber product pattern (for example, "5-Pack Baby Neutral Assorted Bodysuits").
5. Recheck both themes and the phone layout.
