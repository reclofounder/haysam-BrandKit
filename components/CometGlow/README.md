# CometGlow

The warm comet: a crisp `yellow` head and a soft `fire` trail, aimed at the hero.

## When to use

On `night` covers (night and cinema moods), or on lavender as the "Lavanda + comet" look. Counts toward the one-or-two signature details per design.

## Markup

```html
<div style="position: relative; overflow: hidden">
  <div class="hs-comet" style="width: 1400px; left: -560px; top: 330px; --hs-comet-angle: 18deg"></div>
  ...
</div>
```

- `hs-comet` is absolutely positioned; place and size it with `left`, `top` and `width`. The head points right at 0°; rotate with `--hs-comet-angle` until the head aims at the hero.
- For final artwork use the image files: `assets/Elements/haysam-comet-warm.png` (transparent) or the full backgrounds in `assets/Backgrounds/haysam-bg-glow-*`. The CSS version is for layouts and previews.
- The sky comet (`assets/Elements/haysam-comet-sky.png`) is for offers only.

## Do and don't

- Always aim the head at the hero; never let the comet point away from the content.
- Keep text off the brightest part of the head.
