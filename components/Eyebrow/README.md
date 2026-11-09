# Eyebrow

Two small labels: the eyebrow badge above a hero title, and the kicker above a section or panel.

## Markup

```html
<p class="hs-eyebrow caption-1"><i class="hs-i hs-i--puzzle-piece" aria-hidden="true"></i> Claude uchun plagin</p>
<p class="hs-kicker caption-3">Tayyor brif</p>
```

- Eyebrow: white pill (`surface`, `line` border, `radius-full`), `text-muted` label in `caption-1`, an optional Phosphor icon in `ink`. One per page, above the hero title.
- Kicker: `caption-3` in `ink`, caps, 0.06em letter spacing. Use it to name a section ("Muammo") or a panel ("Siz yozasiz", "Tayyor brif"), 12px above the title it introduces.

## Do and don't

- Two to four words.
- Not a status badge: there are no coloured status pills in this system yet.
