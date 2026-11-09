# Hero

The opening block of a page: eyebrow, gradient title, lead paragraph, one primary action and a proof line.

## When to use

The top of a landing or product page, once per page. Inner app screens start with a plain `heading-3` title instead.

## Markup

```html
<section class="hero">
  <p class="hs-eyebrow caption-1"><i class="hs-i hs-i--puzzle-piece" aria-hidden="true"></i> Claude uchun plagin</p>
  <h1 class="heading-1 hs-gradient-text">Instagram muqovasi bitta gapdan</h1>
  <p class="body-3 hs-muted">Sarlavha, tool va kayfiyatni yozasiz.</p>
  <a class="hs-btn hs-btn--primary button-lg" href="...">Plaginni o'rnatish <i class="hs-i hs-i--arrow-down" aria-hidden="true"></i></a>
  <p class="caption-2 hs-muted">15 ta layout · 9:16 va 4:5 birga · API kalitsiz</p>
</section>
```

- Centred; title and lead at most `measure` (680px) wide.
- Spacing: 24px (`s-300`) between eyebrow, title and lead; 32px (`s-400`) above the button; 16px (`s-200`) above the proof line. Page top padding 160px under the floating nav.
- `hs-gradient-text` runs `hero-from` to `hero-to` (black to grey), left to right. Use it on the hero title only.
- `heading-1` steps down to 48/48 below 720px.
