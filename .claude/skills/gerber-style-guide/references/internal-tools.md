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

## The Warehouse Order Assistant (`index.html`)

The prototype follows this guide (applied 2026-10-01, with a second, more visible brand pass the same day). Use it as the reference for how the guide looks in a working tool.

- The tokens are inlined at the top of its `<style>`, because GitHub Pages doesn't serve the `.claude/` folder. If you change `tokens.css`, copy the change there too.
- Montserrat is used throughout. Headings are 400, and labels are uppercase 600 with 0.05em tracking. IBM Plex Mono is used for order numbers, SKUs, IDocs and bin locations.
- Primary buttons (New issue, Send, Send escalation) are square, navy and uppercase. Chips, cards and inputs use the 6px tool radius.
- The prototype banner uses the Maize solid with navy text.
- The header is the navy inverse section with cream text. It carries a text wordmark, "Gerber® Childrenswear", as an eyebrow above the tool name. There's no logo file.
- Pastel tints mark areas, one family each: Jordy for suggestions, the active issue and the demo guide; Geraldine for the diagnosis card head; Maize for the escalation modal head; Seanymph for resolved actions.
- Mock items follow the Gerber product-name pattern.
