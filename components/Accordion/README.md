# Accordion

Questions that open to show an answer, built on native `details` and `summary`.

## When to use

FAQs and optional detail that most people skip. Not for required steps or form sections.

## Markup

```html
<div class="hs-accordion">
  <details><summary class="title-2">API kalit kerakmi?</summary><p class="body-6">Yo'q. ...</p></details>
</div>
```

- Each item: `surface`, 1px `line` border, `radius-md`, 16px × 24px padding, 8px between items; at most `measure-wide` (760px) wide.
- Question in `title-2`; answer in `body-6` `text-muted`, 12px below.
- The `+` marker turns 45° to `×` when open (500ms, `--ease`).
