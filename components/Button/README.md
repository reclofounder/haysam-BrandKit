# Button

The brand-book pill: a rounded ink button with a JetBrains Mono label, for downloads and links on pages, decks and documents.

## When to use

Web pages, the brand book, slides: anywhere a reader clicks. On social posts use `PopButton` or `GlassCTA` instead.

## Markup

```html
<a class="hs-button" href="...">SVG <span aria-hidden="true">↓</span></a>
<a class="hs-button hs-button--lg" href="...">Barcha shriftlar · ZIP <span aria-hidden="true">↓</span></a>
<a class="hs-button hs-button--yellow hs-button--lg" href="...">AI brief · .md <span aria-hidden="true">↓</span></a>
```

- Default: `button` fill with `on-button` label: ink with white text on Lavender, yellow with ink text on Night.
- `hs-button--yellow`: the yellow pill on any ground, for the one primary action.
- `hs-button--lg`: 18px label.
- Focus shows a 3px `fire` ring.

## Do and don't

- Label with what happens or what you get, plus `↓` for downloads or `→` for links. No emoji.
- Keep one yellow button per view.
