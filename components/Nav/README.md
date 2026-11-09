# Nav

The floating glass navigation bar: app icon and product name, page links, one primary action; a menu button below 720px.

## When to use

The top of every product page and website, fixed 16px from the top and centred.

## Markup

```html
<header class="hs-nav-wrap">
  <nav class="hs-nav" aria-label="Asosiy menyu">
    <a class="hs-nav__brand" href="/"><span class="hs-app-icon" aria-hidden="true"></span><span class="title-3">Haysam Cover</span></a>
    <ul class="hs-nav__links"><li><a class="body-5" href="#qanday">Qanday ishlaydi</a></li></ul>
    <a class="hs-btn hs-btn--primary button-sm hs-nav__cta" href="#ornatish">O'rnatish</a>
    <button class="hs-menu-toggle" type="button" aria-expanded="false" aria-controls="menu" aria-label="Menyu"><span></span><span></span></button>
  </nav>
  <div class="hs-mobile-menu" id="menu" hidden>...</div>
</header>
```

- Bar: `glass` fill with a 16px backdrop blur (`blur-nav`), 1px `line` border, `radius-lg`.
- Brand: the 24px app icon (`assets/Marks/haysam-app-icon.svg`, class `hs-app-icon`) and the product name in `title-3`. For the main platform the full logo (`hs-logo--ink` at 24px tall) also works.
- Links: `body-5` in `text-muted`, `text` on hover and for the current page (`aria-current="page"`).
- Below 720px links and the action hide and `hs-menu-toggle` appears; it opens `hs-mobile-menu` (full screen, `glass-menu`, 24px blur) with links in `heading-4`. You provide the toggle script.
- Footer: `hs-footer`, a `line` rule above `caption-2` text in `text-muted`.
