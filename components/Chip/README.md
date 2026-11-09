# Chip

Pill-shaped single- or multi-choice options: muted on the tinted background at rest, solid ink when selected.

## When to use

Choosing one or a few options from a short list (2 to 8) in a form: post type, format, image source. For switching views use `Tabs`; for long lists use a select.

## Markup

```html
<fieldset class="hs-field">
  <legend class="body-4">Post turi</legend>
  <div class="hs-chips">
    <label class="hs-chip"><input type="radio" name="type" value="lesson" checked><span class="button-sm">Yangi darslik</span></label>
    <label class="hs-chip"><input type="radio" name="type" value="offer"><span class="button-sm">Aksiya</span></label>
  </div>
</fieldset>
```

- Use `type="radio"` for one choice and `type="checkbox"` for several. The input stays in the DOM for keyboard and screen readers; the span is what people see.
- Rest: `background` fill, `line` border, `text-muted` label. Hover: `text` label. Selected: `primary` fill and border, `on-primary` label. Keyboard focus: 2px `focus` ring.
- Gap between chips is `s-75`; label text is `button-sm`.

## Do and don't

- Keep labels short; a middle dot can add a detail ("Muqova · 9:16 va 4:5").
- Don't use chips as decoration or status tags; the post chip with a fire dot (`PostChip`) is media only.
