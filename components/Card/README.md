# Card

A white, line-bordered block with 24px padding, for features, summaries and anything that sits in a grid.

## When to use

Grids of features, lessons, courses or settings groups. Larger containers (forms, output, install steps) use `hs-panel` (24px radius); a tinted group inside a panel uses `hs-inset`.

## Markup

```html
<article class="hs-card">
  <span class="hs-icon-tile"><i class="hs-i hs-i--lightbulb" aria-hidden="true"></i></span>
  <h3 class="title-1">G'oya ma'nodan</h3>
  <p class="body-6">Sarlavha va bitta gapdan metafora topadi.</p>
</article>
```

- `surface` fill, 1px `line` border, `radius-lg`, `s-300` padding, `s-75` gap. Title in `title-1`, text in `body-6` (`text-muted`).
- Icon tile: 40px, `icon-bg` (soft yellow), `radius-sm`, a 24px Phosphor icon in `ink`.
- Cards lift 2px on hover. Lay them out with `hs-grid` (16px gap).
- Borders, not shadows: cards have no shadow.
