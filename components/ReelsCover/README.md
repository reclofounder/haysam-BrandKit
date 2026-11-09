# ReelsCover

A 1080×1920 Reels and Stories cover, shown here as a tool hero on `night` with the comet, and again with the safe band and Reels UI zones overlaid.

## When to use

Every Reels or Stories cover. It is the master: the 4:5 feed crop (1080×1350) and the 3:4 profile grid are cut from it.

## What you provide

- The logo, or the `ToolLockup` for a tool post, centred at about y 330.
- One headline (two lines at most) and at most one supporting element, all inside y 285–1635.
- A ground: lavender, `night` with the comet glow (night and cinema moods only), or a full-bleed AI image.

## Markup

```html
<div class="hs-artboard hs-artboard--story" data-theme="night" style="background: var(--canvas)">
  ...
  <div class="hs-guides" aria-hidden="true">
    <div class="hs-guides__safe"></div>
    <div class="hs-guides__ui-right"></div>
    <div class="hs-guides__ui-bottom"></div>
  </div>
</div>
```

`hs-guides` draws the safe band (`safe-top`–`safe-bottom`) and hatches the Reels UI zones; remove it before export.

## Do and don't

- Never put text in the right 140px below y 1180 or in the bottom 330px.
- Size the headline to fit 936px (184px for `VEO’DA VIDEO / YASASH` in Big Shoulders Display).
