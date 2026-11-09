# PopButton

A big, glossy call to action for posts, with a rim and glow in the button's own hue.

## When to use

As a signature detail on a cover or slide that asks for one action. Counts toward the one-or-two signature details per design.

## Markup

```html
<span class="hs-pop">Darsni ko‘rish</span>
<span class="hs-pop hs-pop--fire">Boshlash</span>
```

- Default: `yellow` with ink text and `shadow-pop-yellow`.
- `hs-pop--fire`: `fire` with white text and `shadow-pop-fire`. Use only when fire is the design's accent.
- Label set in Archivo Black (`loud`) at 56px on a 1080px canvas; change `font-size` to scale the whole button.

## Do and don't

- Never give it a dark outline, bevel or drop shadow in another colour.
- Match the button to the design's single accent.
