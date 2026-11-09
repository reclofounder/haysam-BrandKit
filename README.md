# Haysam Design System

Haysam is an Uzbek AI-education platform: lessons, tutorials, news about AI tools and special offers, for adults who want to work faster with AI. This repository is its design system: colour and type tokens, the official logo files, fonts, backgrounds, component recipes and the rules that keep every post on-brand.

## Use it in Claude Design

**Ready-made system:** open [Haysam in Claude Design](https://claude.ai/artifact/Ht4CLwrMEiWZxMPMbijf8z) and design with it directly.

**Or build your own copy from this repository:**

1. Open [Claude Design](https://claude.ai/design) and start a new design system.
2. Add this repository as the source: `https://github.com/reclofounder/haysam-BrandKit`. If GitHub isn't connected, download the ZIP (**Code → Download ZIP**), unzip it and drop the folder in instead.
3. Claude reads `tokens.json`, `fonts/`, `assets/`, `components/` and this README, and builds the Haysam system from them. `tokens.json` is already in Claude Design's format, so colours, type, spacing, radii and shadows come across exactly.
4. Design with it: ask for a Reels cover, a carousel, a slide or a landing page "in the Haysam design system".

**Other tools**

- **Claude Code and other agents:** clone the repo; `SKILL.md` tells an agent how to use it.
- **Web pages:** link `tokens.css`, then `components/bundle.css`, and use the `hs-` classes.
- **Any AI chat (ChatGPT, Gemini, Figma AI):** paste `docs/haysam-brand-brief.md` and attach the logo, font and background files.

## What's inside

| Path | What |
| --- | --- |
| `tokens.json` | Every colour, type style, spacing step, radius, shadow and format measurement, in Claude Design's token format |
| `tokens.css` | The same tokens as CSS custom properties, `@font-face` rules and one class per type style |
| `components/bundle.css` | `hs-` classes for the logo, buttons, chips, stickers, signature details and artboards |
| `components/<Name>/` | A live `preview.html` and a usage `README.md` for each component |
| `fonts/` | The eight brand typefaces (OFL licences in `fonts/licenses/`) |
| `assets/Logos`, `assets/Marks` | Official SVG lockups and marks |
| `assets/Backgrounds`, `assets/Elements` | Lavender and glow backgrounds, comet glows and pattern overlays |
| `exports/logos/` | 6000px PNG (transparent) and JPG exports of every logo |
| `docs/` | The original brand book PDF and the AI brief |
| `scripts/build.mjs` | Rebuilds `tokens.css` and the embedded logos after you edit `tokens.json` or a logo file |

---

## Voice and copy

- Write in Uzbek, Latin script. Write o‘ and g‘ with the ‘ mark, as the brand book does: `ko‘p`, `qo‘llanma`. Never a backtick or a plain apostrophe.
- Sound like a friendly expert: short, direct, specific. One idea per post.
- Every post reads as learning content (a lesson, a how-to, a result), never as an ad for a tool.
- Real examples from the brand book: `5 TA AI VOSITA` / `ishingizni osonlashtiradi`, `VEO’DA VIDEO YASASH`, `Hi Anvar,` / `yangiligimiz bor!`, chip `Bir xil ishlarga ko‘p vaqt ketyaptimi?`.
- Casing follows the mood font: caps for `news`, `cinema`, `brand` and `future` headlines; sentence case for `premium`; `play` may run lowercase.
- No emoji, no filler labels, no fake UI captions, no page counters such as `02 / 07`, no placeholder text, no small meta text.

## Logo

- The only logo is the mark plus the caps HAYSAM wordmark. Always use the files in `assets/Logos` (or the `hs-logo` classes, which embed the same files). Never type the wordmark, redraw it, or generate it. The old lowercase "haysam" logo is retired.
- Pick the file by background:
  - `haysam-logo-ink`: lavender and white grounds. The default. Class `hs-logo--ink`.
  - `haysam-logo-yellow-ink`: light grounds when the design uses the yellow accent. `hs-logo--yellow-ink`.
  - `haysam-logo-yellow-white`: the `night` ground. `hs-logo--yellow-white`.
  - `haysam-logo-white`: on photos and images. `hs-logo--white`.
  - `haysam-logo-black`: one-colour print only. `hs-logo--black`.
  - `hs-logo--auto` switches between ink and yellow-white with the theme.
- On a 1080px-wide canvas the lockup is `logo-height` (52px) tall, centred, near the top (`logo-y`, about y 330 on a 1080×1920 cover).
- Clear space on every side is half the mark's height (`hs-logo-clear`). Smallest size: 32px tall on screen, 20mm wide in print.
- With a tool, set `HAYSAM × [official tool logo] Tool name` on one line (`ToolLockup`).
- Never stretch, rotate, recolour outside the palette, outline, add shadows or effects, or place it on a busy part of an image.
- The mark alone (`assets/Marks`) works as an avatar, app icon, sticker or in small spaces.

## Colour

| Token | Hex | Role |
| --- | --- | --- |
| `lavender` | #E5E9FF | Default canvas, top of the canvas gradient |
| `lavender-white` | #F6F7FF | Bottom of the canvas gradient, boards and carousels |
| `ink` | #58160C | All brand text and the ink logo |
| `night` | #270601 | Dark canvas, night and cinema covers only |
| `yellow` | #FEE252 | Accent: stickers, pop buttons, the comet's head |
| `fire` | #DF3909 | Accent: comet trail, cursor, selection box |
| `white` | #FFFFFF | Cards and tool tiles on lavender; text on night |
| `dot-grid` | #C7CCEB | Dot-grid pattern and hairlines |
| `sky-light` → `sky` → `sky-deep` | #9EE8FF → #2CD3F3 → #1B7BFF | Offer gradient, offers and prices only |
| `night` → `ink` → `metal-light` | #270601 → #58160C → #A0301A | Ink-metal lettering gradient |

- The canvas is a vertical gradient from `canvas` to `canvas-end` (lavender to lavender-white). Use `hs-canvas`, `hs-canvas--dots` or `hs-canvas--lines`.
- Text is `ink` on light grounds and `white` on `night`. The semantic `text` token does this for you in the Lavender and Night themes.
- Use ONE accent per design: `yellow` or `fire`, never both.
- Rough share of a design: canvas 60, ink 25, white 10, accent 5.
- `fire` text is 3.7:1 on lavender: use it for marks, the cursor, eyebrows in bold caps and text 24px or larger, never for small body copy.
- `sky` gradients belong to offers and prices only (`hs-offer-sky`).
- When a design is built on a photo, the photo sets every colour. Haysam then shows only through the logo, the tool logo and the font.
- Never use lime or acid green.

## Type

Pick ONE mood font per post and change it from post to post, so the feed stays lively but familiar.

| Mood | Face | Token / class | Use for |
| --- | --- | --- | --- |
| brand | JetBrains Mono Bold | `--font-brand`, `headline-brand` | The Haysam voice, notes, stickers, code |
| news | Anton | `--font-news`, `headline-news` | News, loud caps |
| future | Unbounded Black | `--font-future`, `headline-future` | Tech, numbers, anything new |
| loud | Archivo Black | `--font-loud`, `headline-loud` | Buttons, hype |
| cinema | Big Shoulders Display Black | `--font-cinema`, `headline-cinema` | Video, film, process |
| premium | Instrument Serif | `--font-premium`, `headline-premium` | Personal letters, calm moments |
| play | Bricolage Grotesque ExtraBold | `--font-play`, `headline-play` | Friendly, community |
| ui | Inter | `--font-ui`, `chip-label` | Chips and labels only |

- Headlines are big: 110 to 230px on a 1080px canvas, two lines at most, line height 88 to 95 percent. Fit the longest line to the text width (936px between the 72px margins) and size down rather than run to a third line.
- One supporting line at most (`subline`, 72px). `chip-label` (32px) is the smallest text on a post.
- Brand-book pages, slides and web pages use `display` (JetBrains Mono ExtraBold caps) for titles, `lead` and `body` (Inter) for text, `label` for buttons and codes, and `eyebrow` for section labels.
- All faces are free Google Fonts under the OFL; the files are in `fonts/`.

## Backgrounds and imagery

- Default: the lavender gradient, plain or with ONE pattern: dots, lines or tiles (`assets/Backgrounds`, or `hs-canvas--dots` / `hs-canvas--lines`).
- Carousel slides always sit on lavender with the dot grid.
- `night` with the warm comet glow is for night and cinema moods only.
- Full-bleed AI image covers fill the whole frame, never a flat colour block on top.
- The comet glow has a direction: a crisp yellow head and a soft fire trail. Aim the head at the hero. Final art uses `assets/Elements/haysam-comet-warm.png` (or `haysam-comet-sky.png` for offers); `hs-comet` is the CSS stand-in.
- 3D objects are glassmorphic, high detail and adult (not toy or cartoon), in one hue family taken from the topic rather than forced into brand yellow. Cut objects out cleanly: no halo, leftover backdrop or dirty shadow.

## Signature details

Use one or two per design, never all of them.

- Comet glow aimed at the hero (`CometGlow`).
- A Figma-style selection box with a cursor named "haysam" (`SelectionBox`).
- A mono sticker tilted −4° (`Sticker`).
- A big pop button with a rim and glow in its own hue, never a dark outline (`PopButton`).
- A liquid-glass CTA, for offers only (`GlassCTA`).
- Gradient lettering with a thin top sheen, never bevels or WordArt (`GradientLettering`).

## Tool logos and icons

- Every tool or brand named in the text gets its real official logo: from Simple Icons, the brand's press kit or site, or Wikimedia Commons. Never generate or redraw a logo. With no official file, write the name instead.
- Tool logos sit in a white `hs-tile` on lavender, or inline in the `ToolLockup`.
- Haysam has no icon set. Buttons use the text arrows `↓` and `→`. Never use emoji as icons.

## Formats

| Format | Size | Rules |
| --- | --- | --- |
| Reels / Stories cover (master) | 1080×1920 | Keep everything important inside `safe-top`–`safe-bottom` (y 285–1635) so the 4:5 feed crop and the 3:4 profile grid still work. No text in the right 140px below y 1180 or in the bottom 330px (Reels UI). |
| Feed post, carousel slide | 1080×1350 | Lavender with the dot grid. One idea per slide: a large headline, a real tool-logo tile when a tool is named, and one object. |

See `ReelsCover` and `CarouselSlide` for working templates, including an overlay of the safe band and Reels UI zones (`hs-guides`).

## Never

- Page counters such as `02 / 07`.
- Decorative emoji, filler labels or fake UI captions.
- Generated, redrawn or lowercase Haysam logos.
- Lime or acid green.
- Bevel or WordArt effects.
- More than one accent colour.
- Text inside the Reels UI zones.
- Placeholder text.

## Before you hand it over

1. Is the logo an official file, in the right variant for the background?
2. Is the main content inside y 285–1635?
3. Is there one mood font and one accent?
4. Are the tool logos real?
5. Is it free of AI slop: no page counters, filler or emoji?
6. Is the copy in Uzbek Latin, short, and does it read as a lesson or a benefit?

---

## Editing the system

Change values in `tokens.json`, or replace a file in `assets/Logos` or `assets/Marks`, then run:

```bash
node scripts/build.mjs
```

It rewrites `tokens.css` and the embedded logo block at the top of `components/bundle.css`. Open any `components/<Name>/preview.html` through a local server (for example `python3 -m http.server`) to check the result.

## Rights

The Haysam name, logos, backgrounds and brand book belong to Haysam. The fonts are free Google Fonts under the SIL Open Font License; each licence is in `fonts/licenses/`.
