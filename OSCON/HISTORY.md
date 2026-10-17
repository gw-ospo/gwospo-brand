# GW OSCON 2027 — Brand Refresh History

How the 2025 GW Open Source Conference identity was moved onto the refreshed GW brand (2026 guidelines) for 2027: Lorena Barba worked on Claude Design with Fable 5 (August 28, 2026) on items 1 through 7. Typography review (item 8) done Oct. 17, 2026, after research for best-match Google fonts.

## 1. Logo: recolor and year change
- **Input:** `GW__OSCON_horizontal_full-color.svg`, the 2025 logo in the old GW secondary colors.
- **Reference:** GW color palette guidelines (communications.gwu.edu/brand-guidelines/color-palette).
- **Actions:**
  - Changed the "5" in "2025" to a "7" by redrawing that one digit in the SVG.
  - Mapped each of the six logo color slots to a color from the new palette: GW Blue, Potomac, Row House, Blue Fog, Blossom and GW Buff.
- **Technical note:** The `<style>` color definitions inside the SVGs did not survive upload. Colors were therefore written as `fill` attributes on each shape, which also makes the files more portable.
- **Output:** `GW_OSCON_horizontal_full-color_2027.svg`, the "verbatim palette" version.

## 2. Format decision
- We agreed to work from SVG sources rather than EPS, because SVG can be edited directly. EPS files should be converted to SVG first (for example in Illustrator or Inkscape).

## 3. Pattern analysis: how the 2025 palette was extended
- **Input:** `GW__OSCON_pattern.svg` (a 7-color tile pattern), a PNG reference, the original `<style>` block and the old brand color table.
- **Findings:**
  - Used unchanged: Green/Teal #008364 and White.
  - Brightened slightly for screen: Red #C9102F → #DA1A32, Yellow #FFC72C → #FFCE34, Green #78BE20 → #62BB46, GW Blue #033C5A → #133A5A.
  - Left out: both Buffs, Light Blue and Light Buff. All the muted tones were removed.
  - Invented: Purple #7337AA. The old palette had no hue between red and blue, and this purple filled that gap at the same saturation as the secondary colors.
  - **The 2025 recipe:** a dark navy anchor, plus white, plus vivid hues spread around the color wheel, plus one invented hue to fill the biggest gap.
- **Applying it to the new palette:** The new palette already has a vivid red, a vivid blue and a cyan. Its gaps are the pale pastels: Parchment, Patina and Blossom. The equivalent move is to deepen those three to the saturation of the secondary colors, rather than invent a hue that doesn't belong to the palette.
- **Options built** (compared in `Pattern Recolor.dc.html`):
  - A, palette verbatim: `GW_OSCON_pattern_2027_A_verbatim.svg`
  - B, extended: `GW_OSCON_pattern_2027_B_extended.svg`
- **Decision:** B (extended), chosen because it conveys the celebratory, community-first mood of OSCON.

## 4. Extended palette
| Slot | Color | Hex |
|---|---|---|
| Anchor | GW Blue | #033C5A |
| Accent | Potomac | #0075C8 |
| Accent | Row House | #EF4343 |
| Extended | OSCON Gold (Parchment deepened) | #FFD34D |
| Extended | OSCON Green (Patina deepened) | #33A56E |
| Extended | OSCON Orchid (Blossom deepened) | #B04A8F |
| Neutral | White | #FFFFFF |

## 5. Logo redone with the extended palette
- Changed the Blue Fog square to Gold, Blossom to Orchid and Buff to Green. GW Blue, Potomac and Row House stayed the same.
- **Output:** `GW_OSCON_horizontal_extended_2027.svg`. Both logo versions can be compared in `Logo Preview.dc.html`.

## 6. Deliverables exported
- Logo: `GW_OSCON_horizontal_extended_2027.svg` and `.png` (2160×792)
- Pattern: `GW_OSCON_pattern_2027_B_extended.svg` and `.png` (4195×1680)
- The PNGs have transparent backgrounds wherever the SVGs have knockout shapes.

## 7. DESIGN.md specification
- **Reference:** GW typography guidelines (communications.gwu.edu/brand-guidelines/typography).
- **Contents:**
  - The core and extended color palettes, with the reasoning behind the extension.
  - Color usage rules, including WCAG AA contrast guidance.
  - Typography: Gazzetta, Avenir Next and Source Serif.
  - Logo and pattern usage, and voice.

## 8. Typography review: Google Fonts substitutes
- Following a user review, the free substitutes were revised:
  - **Source Serif → Source Serif 4.** It is the same Adobe open-source family, with Georgia kept only as a backup if the font fails to load.
  - **Avenir Next → Nunito Sans,** replacing the generic system fonts.
  - **Gazzetta → Barlow Condensed** as the main stand-in, with Oswald only for heavy all-caps display.
- **Added to DESIGN.md:** CSS font stacks, a Google Fonts embed link, a rule never to mix originals and substitutes in one asset, and a note on width differences between the fonts.

## Open items
- There is no reversed logo for dark backgrounds yet.
- The estimate that Barlow Condensed sets about 5% wider than Gazzetta has not been measured. Compare the two fonts side by side.
- Contrast for OSCON Gold, Green and Orchid should be checked in each layout.
