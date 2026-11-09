# SelectionBox

A Figma-style selection box around the hero, with a cursor named "haysam".

## When to use

As a signature detail around a headline word or the hero object, to say "we are designing this with AI". Counts toward the one-or-two signature details per design.

## Markup

```html
<span class="hs-select">
  AI vosita
  <i class="hs-select__h hs-select__h--tl"></i><i class="hs-select__h hs-select__h--tr"></i>
  <i class="hs-select__h hs-select__h--bl"></i><i class="hs-select__h hs-select__h--br"></i>
  <span class="hs-cursor" aria-hidden="true">
    <svg class="hs-cursor__arrow" viewBox="0 0 24 24"><path d="M3 2 21 10.5 13.2 12.8 9.6 20.5Z"/></svg>
    <span class="hs-cursor__name">haysam</span>
  </span>
</span>
```

The box, handles and cursor are `fire`; handles are white squares. The cursor sits at the lower right; set its `font-size` to scale it.

## Do and don't

- The cursor's name is always "haysam", in lowercase.
- One selection per design.
