# Haysam Design System

Haysam is an Uzbek AI-education platform: lessons, tutorials, news about AI tools and special offers, for adults who want to work faster with AI. This repository is its design system, in two layers:

- **Product UI** for app.haysam.school and Haysam websites: clean, structured and flat, taken from [haysam-cover.vercel.app](https://haysam-cover.vercel.app/).
- **Media** art direction for Instagram posts, Reels covers and carousels, from the Haysam brand book.

Both share the logo, the colours ink, yellow and lavender, and the voice.

## Use it in Claude Design

**Ready-made system:** open [Haysam in Claude Design](https://claude.ai/artifact/Ht4CLwrMEiWZxMPMbijf8z) and design with it directly.

**Or build your own copy from this repository:**

1. Open [Claude Design](https://claude.ai/design) and start a new design system.
2. Add this repository as the source: `https://github.com/reclofounder/haysam-BrandKit`. If GitHub isn't connected, download the ZIP (**Code → Download ZIP**), unzip it and drop the folder in instead.
3. Claude reads `tokens.json`, `fonts/`, `assets/`, `components/` and this README, and builds the Haysam system from them. `tokens.json` is already in Claude Design's format, so colours, type, spacing, radii and shadows come across exactly.
4. Design with it: ask for "an app.haysam.school lessons page in the Haysam design system" or "a Haysam Reels cover about Google Veo".

**Other tools**

- **Claude Code and other agents:** clone the repo; `SKILL.md` tells an agent how to use it.
- **Web code:** link `tokens.css`, then `components/bundle.css`, and use the type classes (`heading-1`, `body-3`, `button-md`…) with the `hs-` component classes.
- **Any AI chat (ChatGPT, Gemini, Figma AI) for posts:** paste `docs/haysam-brand-brief.md` and attach the logo, font and background files.

## What's inside

| Path | What |
| --- | --- |
| `tokens.json` | Every colour, type style, spacing step, radius, shadow and layout value, in Claude Design's token format |
| `tokens.css` | The same tokens as CSS custom properties, `@font-face` rules and one class per type style |
| `components/bundle.css` | `hs-` classes: product UI first, media after |
| `components/<Name>/` | A live `preview.html` and a usage `README.md` for each component |
| `fonts/` | Geist and Geist Mono for UI, eight faces for media (OFL licences in `fonts/licenses/`) |
| `assets/Logos`, `assets/Marks` | Official SVG lockups, marks and the app icon |
| `assets/Icons` | The Phosphor Regular icons the UI uses (MIT) |
| `assets/Backgrounds`, `assets/Elements` | Media: lavender and glow backgrounds, comet glows and pattern overlays |
| `exports/logos/` | 6000px PNG (transparent) and JPG exports of every logo |
| `docs/` | The original brand book PDF and the AI brief for posts |
| `scripts/build.mjs` | Rebuilds `tokens.css` and the embedded logos and icons after you edit `tokens.json` or an SVG |

---

# Product UI

For app.haysam.school, haysam.school and every Haysam web tool. The reference is [haysam-cover.vercel.app](https://haysam-cover.vercel.app/): every value here comes from its stylesheet.

## Principles

- **Calm and flat.** A `background` (lavender-white) page, `surface` (white) cards and panels, separated by 1px `line` borders. No shadows, except `shadow-xs` on a selected tab.
- **Ink is the action colour.** Primary buttons and selected chips are `primary` (ink). Everything else is `text`, `text-muted` and white.
- **Yellow is a small highlight.** Only on step numbers, numbered circles (`highlight`) and icon tiles (`icon-bg`). Never a large yellow area in UI.
- **One family.** Geist for all text, Geist Mono for step numbers and code, on the fixed type scale below.
- **One spacing scale.** Every gap and padding is a step of the 4px-based `s-` scale.
- **No media effects in UI.** No mood fonts, comet glows, stickers, tilted elements, pop buttons, dot grids or lavender gradients. Those belong to posts.

## Colour

| Token | Value | Use |
| --- | --- | --- |
| `background` | #F6F7FF | Page background; resting fill of inputs, chips and tab bars |
| `surface` | #FFFFFF | Cards, panels, nav, selected tab, focused input |
| `text` | #140907 | Headings and body text (18.4:1 on background) |
| `text-muted` | #5E5654 | Descriptions, helper text, nav links, captions (6.7:1) |
| `text-placeholder` | #9A9391 | Placeholders only (2.8:1: never for real content) |
| `line` / `line-strong` | #E3E5F3 / #CFD2E6 | 1px borders; input border on hover |
| `primary` / `primary-hover` | #58160C / #6E1E12 | Primary buttons, selected chips; white text on them |
| `highlight` | #FEE252 | Step numbers and numbered circles, with ink text |
| `icon-bg` | #FFF6C9 | Icon tiles, with an ink icon |
| `focus` | #1B7BFF | Focus ring and focused input border |
| `danger` | #B42318 | Error text and invalid borders |
| `success` | #2F6B2A | Done state of copy and save buttons |
| `code-bg`, `code-text`, `code-button` | #1F1F1F, #F6F7FF, #313131 | Code blocks |
| `glass`, `glass-menu` | white 72%, lavender-white 94% | Floating nav and mobile menu, with backdrop blur |
| `hero-from` → `hero-to` | #000000 → #666666 | Hero title gradient, left to right |

## Type

Geist, on this scale (size / line height / weight). Use the class names as written.

| Style | Spec | Use |
| --- | --- | --- |
| `heading-1` | 60/60 600, −0.02em | Hero title (48/48 below 720px) |
| `heading-2` | 48/48 600, −0.02em | Closing call to action, statement lines (36/40 below 720px) |
| `heading-3` | 36/40 600, −0.01em | Section and screen titles (30/36 below 720px) |
| `heading-4` | 30/36 600 | Mobile menu links, large numbers |
| `title-1` | 20/28 500 | Card and step titles |
| `title-2` | 18/28 500 | Accordion questions, list titles |
| `title-3` | 16/24 500 | Product name in the nav, small headings |
| `body-2` / `body-3` | 16/24 500 / 400 | Emphasised text / lead paragraphs and input text |
| `body-4` / `body-5` / `body-6` | 14/20 600 / 500 / 400 | Form labels / nav links / card text and answers |
| `button-lg` / `-md` / `-sm` / `-xsm` | 18/28, 16/24, 14/20, 12/16, all 600 | Button labels by size |
| `caption-1` / `caption-2` | 14/20 500 / 400 | Eyebrow / hints, proof lines, footer |
| `caption-3` / `caption-4` | 12/16 600 / 500 | Kickers and step numbers / image captions |
| `mono-md` / `mono-sm` / `mono-xs` | Geist Mono 14/20, 13/20, 12/16, 500 | Code blocks / text output / inline code |

- Section titles are `heading-3`; a muted `body-6` intro sits 8px under them; content starts 40px below.
- Headings use `text-wrap: balance`, paragraphs `text-wrap: pretty`.

## Spacing, radius and layout

- Spacing: `s-25` 2, `s-50` 4, `s-75` 8, `s-100` 12, `s-200` 16, `s-300` 24, `s-400` 32, `s-500` 40, `s-600` 48, `s-700` 64, `s-800` 80, `s-900` 96 (px).
- Common pairs: buttons and inputs pad 8 × 12; cards and panels pad 24; grids gap 16; form fields gap 24; sections pad 96 top and bottom (80 on mobile) with a 24px side gutter (16 on mobile).
- Radius by size: `radius-xs` 4 (step numbers, inline code), `radius-sm` 8 (icon tiles, tabs), `radius-md` 12 (buttons, inputs, code, accordion items), `radius-lg` 16 (cards, nav), `radius-xl` 24 (large panels), `radius-full` (eyebrows, chips, number circles).
- Widths: sections max `container` (1120px); hero text and simple text pages max `measure` (680px); accordions max `measure-wide` (760px).
- Breakpoints: below `breakpoint-md` (900px) two-column layouts stack; below `breakpoint-sm` (720px) the nav collapses, headings step down and field rows stack.

## Components

| Component | Classes | For |
| --- | --- | --- |
| `Button` | `hs-btn hs-btn--primary` / `--secondary` + `button-*` | Every action |
| `Chip` | `hs-chips`, `hs-chip` | Choosing options in a form |
| `Tabs` | `hs-tabs`, `hs-tab` | Switching parallel views |
| `Input` | `hs-field`, `hs-input`, `hs-select`, `hs-field__hint`, `hs-field__error` | Form fields |
| `Hero` | `hs-eyebrow`, `hs-gradient-text` | Page openings |
| `Eyebrow` | `hs-eyebrow`, `hs-kicker` | Labels above titles |
| `Card` | `hs-card`, `hs-icon-tile`, `hs-panel`, `hs-inset`, `hs-grid` | Grouped content |
| `Steps` | `hs-step-num`, `hs-numbered` | Sequences |
| `CodeBlock` | `hs-code`, `hs-copy`, `hs-code-inline` | Commands to copy |
| `Accordion` | `hs-accordion` | FAQs |
| `Nav` | `hs-nav-wrap`, `hs-nav`, `hs-menu-toggle`, `hs-mobile-menu`, `hs-footer` | Page navigation |

Put `hs-ui` on the page's `body` for the background, text colour, font and focus ring. Each component's `README.md` has its markup and rules.

## Icons

- Phosphor Icons, Regular weight, version 2.1.1. In code, load `@phosphor-icons/web@2.1.1` (regular) and write `<i class="ph ph-copy">`, or use the files in `assets/Icons` through `<i class="hs-i hs-i--copy">`, which draws in the current text colour.
- 18px inside buttons; 24px inside a 40px icon tile, in `ink` on `icon-bg`.
- Arrows show direction: `arrow-down` for install or download, `arrow-up-right` for opening elsewhere. `copy` and `check` for copy and done.
- No emoji as icons, and no third-party logo glyphs: use official logo files.

## Motion

- One curve: `--ease` = `cubic-bezier(0.22, 1, 0.36, 1)`. Colour changes take 300ms, movement 500ms, reveals 700ms.
- Hover lifts buttons 1px and cards 2px; press scales to 0.98; the accordion marker turns 45°.
- Under `prefers-reduced-motion`, remove movement and keep 300ms fades.

## Accessibility

- Focus: a 2px `focus` ring with a 2px offset on every interactive element.
- Contrast: `text` and `text-muted` pass 4.5:1 on `background` and `surface`; white on `primary` is 13.7:1. `text-placeholder` and `line` do not, so they never carry information alone.
- Every input has a visible `body-4` label; hints and errors are linked with `aria-describedby`; invalid fields get `aria-invalid="true"`.
- Chips keep their real radio or checkbox input; tabs use `role="tab"` and `aria-selected`; the menu button sets `aria-expanded`. Provide a skip link (`hs-skip`).

## UI copy

- Uzbek, Latin script. Short and plain: the site's "Qanday ishlaydi", "Brifni shu yerda yozing", "Nusxalash".
- Sentence case for headings, buttons and labels; caps only in kickers.
- Buttons are verbs that say what happens ("Plaginni o'rnatish", "Claude'da ochish"). Done states use the past tense ("Nusxalandi").
- Optional fields say "(ixtiyoriy)" in muted text after the label. Hints are one short sentence.
- UI text uses the plain apostrophe in o', g' and the tutuq belgisi, as the site does (O'rnatish, ko'p, ma'no).
- No emoji, filler or placeholder text.

---

# Logo

Applies to UI and media.

- The only logo is the mark plus the caps HAYSAM wordmark. Always use the files in `assets/Logos` (or the `hs-logo` classes, which embed the same files). Never type the wordmark, redraw it, or generate it. The old lowercase "haysam" logo is retired.
- Pick the file by background:
  - `haysam-logo-ink`: lavender and white grounds. The default. Class `hs-logo--ink`.
  - `haysam-logo-yellow-ink`: light grounds when the design uses the yellow accent. `hs-logo--yellow-ink`.
  - `haysam-logo-yellow-white`: the `night` ground. `hs-logo--yellow-white`.
  - `haysam-logo-white`: on photos and images. `hs-logo--white`.
  - `haysam-logo-black`: one-colour print only. `hs-logo--black`.
  - `hs-logo--auto` switches between ink and yellow-white with the Night theme.
- The app icon (`assets/Marks/haysam-app-icon.svg`, class `hs-app-icon`) is the ink mark on a yellow rounded square: favicon, app icon and the 24px brand mark in the UI nav.
- Clear space on every side is half the mark's height (`hs-logo-clear`). Smallest size: 32px tall on screen, 20mm wide in print. The app icon may go down to 16px as a favicon.
- Never stretch, rotate, recolour outside the palette, outline, add shadows or effects, or place the logo on a busy part of an image.
- The mark alone (`assets/Marks`) works as an avatar, sticker or in small spaces.

---

# Media art direction

For Instagram posts, Reels and Stories covers and carousels. Most of the brand book lives here. None of it goes into product UI.

## Voice and copy

- Write in Uzbek, Latin script. Post headlines write o‘ and g‘ with the ‘ mark, as the brand book does: `ko‘p`, `qo‘llanma`.
- Sound like a friendly expert: short, direct, specific. One idea per post.
- Every post reads as learning content (a lesson, a how-to, a result), never as an ad for a tool.
- Real examples from the brand book: `5 TA AI VOSITA` / `ishingizni osonlashtiradi`, `VEO’DA VIDEO YASASH`, `Hi Anvar,` / `yangiligimiz bor!`, chip `Bir xil ishlarga ko‘p vaqt ketyaptimi?`.
- Casing follows the mood font: caps for `news`, `cinema`, `brand` and `future` headlines; sentence case for `premium`; `play` may run lowercase.
- No emoji, no filler labels, no fake UI captions, no page counters such as `02 / 07`, no placeholder text, no small meta text.

## Colour

| Token | Hex | Role |
| --- | --- | --- |
| `lavender` → `lavender-white` | #E5E9FF → #F6F7FF | Default post canvas, vertical gradient (`canvas` → `canvas-end`) |
| `ink` | #58160C | All post text and the ink logo (`post-text`) |
| `night` | #270601 | Dark canvas, night and cinema covers only (Night theme) |
| `yellow` | #FEE252 | Accent: stickers, pop buttons, the comet's head |
| `fire` | #DF3909 | Accent: comet trail, cursor, selection box |
| `white` | #FFFFFF | Chips and tool tiles on lavender; text on night |
| `dot-grid` | #C7CCEB | Dot-grid pattern |
| `sky-light` → `sky` → `sky-deep` | #9EE8FF → #2CD3F3 → #1B7BFF | Offer gradient, offers and prices only |
| `night` → `ink` → `metal-light` | #270601 → #58160C → #A0301A | Ink-metal lettering gradient |

- Use ONE accent per design: `yellow` or `fire`, never both.
- Rough share of a design: canvas 60, ink 25, white 10, accent 5.
- `fire` text is 3.7:1 on lavender: use it for marks and text 24px or larger only.
- When a design is built on a photo, the photo sets every colour. Haysam then shows only through the logo, the tool logo and the font.
- Never use lime or acid green.

## Type

Pick ONE mood font per post and change it from post to post, so the feed stays lively but familiar.

| Mood | Face | Class | Use for |
| --- | --- | --- | --- |
| brand | JetBrains Mono Bold | `headline-brand` | The Haysam voice, notes, stickers |
| news | Anton | `headline-news` | News, loud caps |
| future | Unbounded Black | `headline-future` | Tech, numbers, anything new |
| loud | Archivo Black | `headline-loud` | Buttons, hype |
| cinema | Big Shoulders Display Black | `headline-cinema` | Video, film, process |
| premium | Instrument Serif | `headline-premium` | Personal letters, calm moments |
| play | Bricolage Grotesque ExtraBold | `headline-play` | Friendly, community |
| label | Inter | `post-chip-label` | Chips and labels on posts only |

- Headlines are big: 110 to 230px on a 1080px canvas, two lines at most, line height 88 to 95 percent. Fit the longest line to the 936px text width (`post-margin` 72px each side) and size down rather than run to a third line.
- One supporting line at most (`subline`, 72px). `post-chip-label` (32px) is the smallest text on a post.

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

## Tool logos

- Every tool or brand named in the text gets its real official logo: from Simple Icons, the brand's press kit or site, or Wikimedia Commons. Never generate or redraw a logo. With no official file, write the name instead.
- On posts, tool logos sit in a white `hs-tile` on lavender, or inline in the `ToolLockup` (`HAYSAM × [logo] Name`).

## Formats

| Format | Size | Rules |
| --- | --- | --- |
| Reels / Stories cover (master) | 1080×1920 | Keep everything important inside `safe-top`–`safe-bottom` (y 285–1635) so the 4:5 feed crop and the 3:4 profile grid still work. No text in the right 140px below y 1180 or in the bottom 330px (Reels UI). Logo 52px tall, centred near y 330. |
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

## Before you hand over a post

1. Is the logo an official file, in the right variant for the background?
2. Is the main content inside y 285–1635?
3. Is there one mood font and one accent?
4. Are the tool logos real?
5. Is it free of AI slop: no page counters, filler or emoji?
6. Is the copy in Uzbek Latin, short, and does it read as a lesson or a benefit?

---

## Editing the system

Change values in `tokens.json`, or replace an SVG in `assets/Logos`, `assets/Marks` or `assets/Icons`, then run:

```bash
node scripts/build.mjs
```

It rewrites `tokens.css` and the generated block (logos, app icon, icons) at the top of `components/bundle.css`. Open any `components/<Name>/preview.html` through a local server (for example `python3 -m http.server`) to check the result.

## Rights

The Haysam name, logos, backgrounds and brand book belong to Haysam. The fonts are under the SIL Open Font License (`fonts/licenses/`); the Phosphor icons under the MIT License (`assets/Icons/LICENSE-phosphor.txt`).
