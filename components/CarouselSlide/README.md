# CarouselSlide

A 1080×1350 feed or carousel slide on lavender with the dot grid: logo, chip, one big headline, one supporting line, tool tiles and one object.

## When to use

Every carousel slide and 4:5 feed post. Carousel slides always use the lavender canvas with the dot grid.

## What you provide

- One idea, as a headline in one mood font (two lines at most) and an optional subline.
- The official logo of each tool named, in an `hs-tile` (with no official file, the name in the tile).
- One 3D object for the open centre: glassmorphic, high detail, adult, cut out cleanly, in a hue family from the topic.

## Markup

```html
<div class="hs-artboard hs-artboard--feed hs-canvas--dots">
  <!-- logo 64px from the top, centred; then chip, headline, subline -->
  <span class="hs-tile"><img src="openai.svg" alt="ChatGPT"></span>
</div>
```

See `preview.html` for the full layout. `hs-artboard` is 1080px wide; set `--hs-scale` to display it smaller.

## Do and don't

- Size the headline so its longest line fits the 936px text width (172px for `5 TA AI VOSITA` in Anton).
- No page counters (`02 / 07`), emoji or filler.
