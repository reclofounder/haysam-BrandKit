# Steps

Numbered sequences: step cards with a yellow mono number, and a numbered list with yellow circles.

## When to use

A real sequence the reader follows in order: onboarding, installation, how a lesson works. Not for unordered features (use `Card`).

## Markup

```html
<li class="hs-card"><span class="hs-step-num caption-3">01</span><h3 class="title-1">Plaginni o'rnating</h3><p class="body-6">...</p></li>

<ol class="hs-numbered">
  <li><p class="body-4">Plaginni o'rnating</p><p class="body-6 hs-muted">...</p></li>
</ol>
```

- Step number: `highlight` (yellow) fill, `ink` text in Geist Mono `caption-3`, `radius-xs`, two digits.
- Numbered list: 24px `highlight` circles with the number in Geist Mono 12px SemiBold; items 24px apart, text indented 40px. Put code blocks and buttons inside an item when the step needs them.
- Yellow appears in UI only here and in icon tiles: keep it small.
