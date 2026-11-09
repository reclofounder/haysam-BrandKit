---
name: haysam-design-system
description: The Haysam design system. Use when designing or building anything for Haysam, the Uzbek AI-education platform - app.haysam.school screens, Haysam websites and web tools (product UI), or Instagram posts, Reels covers and carousels (media) - so it uses the official logos, tokens, fonts, components and rules.
---

# Haysam design system

Read `README.md` first. It has two layers; decide which one the task is:

- **Product UI** (app.haysam.school, websites, web tools): flat and structured. Geist type scale, `background` page, `surface` cards with 1px `line` borders, ink `primary` buttons, yellow only for step numbers and icon tiles. Reference: haysam-cover.vercel.app.
- **Media** (posts, covers, carousels): lavender canvas, one mood font and one accent per post, signature details, 1080px formats.

Never mix them: no mood fonts, comets, stickers, pop buttons or dot grids in product UI.

## Files to use

- Tokens: `tokens.css` (CSS custom properties, `@font-face`, one class per type style such as `heading-3`, `body-6`, `button-md`) or `tokens.json` (the same values as data).
- Components: `components/bundle.css` gives `hs-` classes. Each `components/<Name>/README.md` has the markup and rules; `preview.html` is a working example. UI: Button, Chip, Tabs, Input, Hero, Eyebrow, Card, Steps, CodeBlock, Accordion, Nav. Media: Logo, ToolLockup, PostChip, Sticker, PopButton, GlassCTA, SelectionBox, CometGlow, GradientLettering, CarouselSlide, ReelsCover.
- Logos and app icon: `assets/Logos`, `assets/Marks`, or the `hs-logo--*`, `hs-mark--*` and `hs-app-icon` classes. Never type, redraw or generate the logo.
- Icons (UI): Phosphor Regular 2.1.1, via `assets/Icons` and `hs-i hs-i--<name>`.
- Fonts: `fonts/`. Media backgrounds and comets: `assets/Backgrounds`, `assets/Elements`.

## Product UI rules

1. Put `hs-ui` on the body. Text is `text`, secondary text `text-muted`, page `background`, cards `surface`.
2. Use only the type scale classes and the `s-` spacing steps; radii by size (`radius-md` controls, `radius-lg` cards, `radius-xl` panels, `radius-full` pills).
3. One primary button per view; buttons always pair `hs-btn` with a `button-*` size class.
4. Every field has a visible label, a linked hint or error, and a 2px `focus` ring.
5. Copy in Uzbek Latin, sentence case, verbs on buttons, "(ixtiyoriy)" for optional fields, no emoji.

## Media rules

1. Copy in Uzbek Latin, short, reading as a lesson or a benefit.
2. Logo: official file, right variant for the ground, 52px tall on a 1080px canvas, centred near the top.
3. One mood font per post, one accent (`yellow` or `fire`) per design.
4. Headlines 110-230px on a 1080px canvas, two lines at most.
5. 1080×1920 covers keep content inside y 285-1635 and out of the Reels UI zones; carousels are 1080×1350 on lavender with the dot grid.
6. Every named tool gets its real official logo. Never lime or acid green, bevels, WordArt, page counters or emoji.

Run the checklist at the end of `README.md` before handing a post over.
