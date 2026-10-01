# Brand: visual identity

These values were read from the gerberchildrenswear.com Shopify theme on 2026-10-01. The token names are in `../tokens.css`.

## Color

### Core

| Token | Hex | Role |
|---|---|---|
| `--gcw-navy` | `#002744` | The brand color. Body text, headings, primary buttons, the logo, the inverse section ground |
| `--gcw-navy-70` | `#2F4E65` | Secondary text on light grounds |
| `--gcw-cream` | `#F9F5F3` | Default page ground (site "scheme 1"), text on navy |
| `--gcw-white` | `#FFFFFF` | Cards and alternate sections (site "scheme 2") |
| `--gcw-mist` | `#F2F4F8` | Form-field fill |
| `--gcw-line` | `#E6E8EC` | Borders and dividers |
| `--gcw-slate` / `--gcw-butter` | `#515D64` / `#FEF9E3` | Alternate pairing used for some promo sections |

### Pastels

The site names its color schemes after these colors. Each comes as a full shade, used for buttons, banners and accents, and a light tint, used for section and card grounds. **Text on all of them is navy.**

| Name | Full | Tint | Navy text on full / tint |
|---|---|---|---|
| Jordy (blue) | `#85B7EA` | `#CEE2F7` | 7.3 : 1 / 11.5 : 1 |
| Maize (yellow) | `#F2C94C` | `#FCF4DB` | 9.6 : 1 / 13.9 : 1 |
| Geraldine (coral) | `#F28C82` | `#FCE8E6` | 6.4 : 1 / 13.0 : 1 |
| Seanymph (sage) | `#86B3A1` | `#E7F0EC` | 6.5 : 1 / 13.2 : 1 |
| Sandy Brown (apricot) | `#F4A261` | `#FDECDF` | 7.4 : 1 / 13.3 : 1 |
| Lavender | `#8A75D1` | — | Accent button only, with white text |

How the site pairs them: a tint section ground carries a full-shade button with navy text (for example, a Maize tint section with a Maize button). A full-shade ground carries a navy button with cream text. Use one pastel family per section or screen. Don't put several pastels next to each other unless it's a deliberate rainbow moment, such as a size or age picker.

### Retail badges

| Badge | Hex | Note |
|---|---|---|
| Sale | `#C4301C` | White text, 5.6 : 1. Also the cart count bubble |
| New | `#359679` | White text is **3.6 : 1, which fails AA for small text**. Use it at large or bold sizes only. For text, use `--ok` `#23705A` |
| Coming soon | `#7A34D6` | White text, 6.4 : 1 |
| Sold out | `#ADADAD` | Fill only |

## Typography

- **Family:** Montserrat for everything: headings, body, navigation, buttons and prices. Load it from Google Fonts with a fallback of `"Helvetica Neue", Arial, system-ui, sans-serif`.
- **Headings:** weight **400**, no letter-spacing, sentence or title case. Sizes on desktop: H1 44px, H2 35px, H3 31px, H4 24px, H5 20px, H6 18px. On mobile, scale them by 0.77. Large display headlines (around 57px) may be uppercase.
- **Subheadings and eyebrows:** uppercase, weight 600, 0.05em tracking, about 15px.
- **Body:** 14px, weight 400, line height 1.575. Bold is 600, bolder is 700.
- **Navigation:** weight 500.
- **Product cards:** title 500 at about 12.5px. Price 600.
- **Numbers:** in data-heavy views, use `font-variant-numeric: tabular-nums`. In internal tools, use the mono face for codes (see `internal-tools.md`).

## Shape and components

- **Corners:** radius 0 on buttons, inputs, badges and cards. Square corners are part of the look.
- **Buttons:** 44px tall, uppercase, Montserrat 600, 0.02em tracking, 1px border.
  - Primary: navy fill with cream text.
  - Secondary: a 1px navy outline with navy text, or a pastel fill with navy text.
  - Inverse (on navy): cream fill with navy text.
- **Inputs:** a 1px border or a mist fill, square corners, navy text. The search field uses a 2px border.
- **Page width:** content maxes out at 1440px.
- **Trademark superscript:** ®, ™ are 0.5em, raised 0.35em, with `line-height: 0` (class `.gcw-tm`) so they don't push lines apart.

## Imagery and logo

- Photography is bright and natural-light: real babies and toddlers, parents' hands, soft neutral or pastel backdrops. There are no heavy filters and no dark moody scenes.
- The logo is the navy "Gerber Childrenswear" wordmark. The site's file is `GerberChildrenswear-Logo-Navy.png`, served from the site CDN. **Ask Gerber marketing for official logo files.** Don't copy the file out of the site or redraw it, and don't recreate or caricature the Gerber Baby. In prototypes, use a plain text label or no logo at all.
- Don't use emoji as brand decoration.

## Sources

- Homepage and theme CSS: https://www.gerberchildrenswear.com (Shopify theme, color schemes `scheme-1` to `scheme-14` and named schemes jordy, maize, geraldine, seanymph and sandybrown), read 2026-10-01.
- About Us: https://www.gerberchildrenswear.com/pages/about-us
- Contrast ratios computed with the WCAG 2.x relative luminance formula.
