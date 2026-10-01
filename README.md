# Warehouse Order Assistant (UI prototype)

A clickable prototype of a chat assistant for warehouse staff. The user describes a problem with an order, answers a few clarifying questions, and gets a diagnosis of where SAP and Deposco disagree, plus step-by-step instructions to fix it. If they can't fix it themselves, the assistant drafts an escalation ticket for the right system owner.

The prototype exists to align on the end-state experience before the real agent is built. **All orders, SKUs, customers and responses are fictional and scripted.** Nothing connects to SAP or Deposco, and escalations aren't sent anywhere.

## Run it

**Live:** https://cjensen-gerber.github.io/UI-prototype/ (GitHub Pages, served from `main`, public link)

To run it locally, open `index.html` in any modern browser. It's a single file with no build step and no backend. It loads fonts from Google Fonts and falls back to system fonts when offline.

## Teams version

`teams.html` shows the same assistant as a Microsoft Teams app. It's live at https://cjensen-gerber.github.io/UI-prototype/teams.html, and the banner on each page links to the other version. It uses the same five mock orders and scripts, plus what Teams adds:

- A 1:1 chat with the **Order Assistant** app. Answers are Adaptive Card-style cards, and the assistant's questions come with suggested replies above the message box.
- Escalations open a Teams dialog and post a card to the owner team's channel under **Warehouse support** (Quality holds, SAP order support, Deposco admin, Shift leads).
- Open that channel to play the system owner. **Assign to me** and **Mark fixed** send updates back to the warehouse user's chat, Activity feed and a notification.
- Under 700px wide it switches to a Teams mobile layout with bottom navigation.

Teams controls fonts and colors inside the client and in cards, so the Gerber brand shows only through the app icon, name, copy and the prototype banner. The Teams chrome is a neutral look-alike with no Microsoft logos.

## Demo script

Type one of these, or tap the suggestions on the start screen. The **Demo guide** button in the yellow banner shows the same list.

| Order | What the user says | Root cause the assistant finds | Ends with |
|---|---|---|---|
| SO-100412 | "Can't find SO-100412 in Deposco" | Outbound IDoc failed (status 51) on a record lock | Shift lead resends the IDoc |
| SO-100437 | "SO-100437 won't allocate" | 36 EA on inspection hold in Deposco, unrestricted in SAP | **Escalation** to the Quality team |
| SO-100455 | "Pick qty looks wrong on SO-100455" | Pack unit (1 PK = 5 EA) missing in Deposco item master | Assistant re-runs the item sync (simulated), user re-allocates |
| SO-100468 | "Packing slip doesn't match SO-100468" | Order changed in SAP after wave release; Deposco rejected the change | Remove from wave, resend change, re-wave |
| SO-100479 | "Label won't print for SO-100479" | Postal code corrected in SAP only | User fixes the ship-to and reprints |

To show the clarifying questions, describe the problem without an order number (e.g. "the shipping label won't print"). If you type something the assistant doesn't recognise, it asks which of the five problems is closest.

The sidebar has three earlier conversations (two resolved, one escalated) to show the issue history.

## Style guide

Brand rules for Gerber work in this repo live in a Claude Code skill at [`.claude/skills/gerber-style-guide/`](.claude/skills/gerber-style-guide/SKILL.md):

- `tokens.css`: colors, type and shape as CSS variables, in light and dark
- `references/brand.md`: palette, typography, components, logo and imagery rules
- `references/voice.md`: tone, trademark rules (Onesies® Brand) and product and size naming
- `references/internal-tools.md`: how to adapt the retail brand for operational tools like this one

Claude Code loads the skill automatically when you work on Gerber assets in this repo. It's built from Gerber's public website, not the official brand book. Official guidelines go in `references/official/` and take precedence.

## What to align on with the customer

- Which mismatch types matter most, and what the real top 5 are by volume
- Which fixes warehouse users may do themselves, and which need SAP, Deposco or Quality owners
- Whether the assistant should take actions itself (like the simulated item resync) or only give instructions
- Where escalations should go (ticketing tool, Teams channel, email) and what they must include
- Devices on the floor: desktop, handheld scanner, tablet
