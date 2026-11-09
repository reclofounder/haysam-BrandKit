---
name: haysam-design-system
description: The Haysam brand design system. Use when designing anything for Haysam, the Uzbek AI-education platform - Instagram Reels and Stories covers, feed posts, carousels, slides, web pages or any visual - so it uses the official logos, colours, fonts, backgrounds and rules.
---

# Haysam design system

Read `README.md` first: it is the brand book (voice, logo, colour, type, backgrounds, signature details, formats, the Never list and the pre-flight checklist). Follow it exactly.

## Files to use

- Tokens: `tokens.css` (CSS custom properties, `@font-face`, one class per type style) or `tokens.json` (the same values as data).
- Components: `components/bundle.css` gives `hs-` classes. Each `components/<Name>/README.md` says when to use it and the markup; `preview.html` is a working example.
- Logos: `assets/Logos/*.svg`, `assets/Marks/*.svg`, or the `hs-logo--*` / `hs-mark--*` classes, which embed the same files. Never type, redraw or generate the logo.
- Fonts: `fonts/` (eight OFL faces). Backgrounds: `assets/Backgrounds/`. Comets and pattern overlays: `assets/Elements/`.

## The rules that matter most

1. Copy in Uzbek Latin, short, reading as a lesson or a benefit. No emoji, page counters, filler or placeholder text.
2. Logo: an official file, the right variant for the ground (ink on light, yellow-white on `night`, white on photos), 52px tall on a 1080px canvas, centred near the top.
3. One mood font per post, one accent (`yellow` or `fire`) per design, ink text on lavender.
4. Headlines 110-230px on a 1080px canvas, two lines at most, line height 0.88-0.95.
5. 1080×1920 covers keep content inside y 285-1635 and out of the Reels UI zones; carousels are 1080×1350 on lavender with the dot grid.
6. Every named tool gets its real official logo; never generate one.
7. Never lime or acid green, bevels, WordArt, or more than one accent.

Run the six-question checklist at the end of `README.md` before handing a design over.
