# Input

Text inputs, textareas and selects with a label above, an optional hint or error below.

## When to use

Every form field in the platform. Group fields in an `hs-panel hs-form` (24px gap between fields); put two short fields side by side with `hs-field-row`.

## Markup

```html
<div class="hs-field">
  <label class="body-4" for="f-headline">Sarlavha</label>
  <input class="hs-input body-3" id="f-headline" placeholder="Saytni o'zing yig'" aria-describedby="f-headline-hint">
  <p class="hs-field__hint caption-2" id="f-headline-hint">Beshta so'zgacha.</p>
</div>
<select class="hs-input hs-select body-3">...</select>
<textarea class="hs-input body-3" rows="2"></textarea>
```

- Label: `body-4` in `text`. Optional fields add `<span class="hs-muted">(ixtiyoriy)</span>` to the label.
- Field: `background` fill, `line` border, `radius-md`, 8px × 12px padding, `body-3` text. Hover: `line-strong` border. Focus: `focus` border and `surface` fill.
- Placeholder: `text-placeholder`, which is light (2.8:1), so never put needed information only in a placeholder.
- Hint: `hs-field__hint caption-2`. Error: `aria-invalid="true"` on the field (`danger` border) and an `hs-field__error caption-2` message linked with `aria-describedby`.
- Inside a tinted `hs-inset` group, fields switch to a `surface` fill.

## Do and don't

- Write errors that say what to do: "Havola to'liq emas: fayl manzilini butunlay nusxalang."
- Keep labels short nouns; put the explanation in the hint.
