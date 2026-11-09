# Button

The product UI button: Geist SemiBold on a 12px-radius block, ink for the main action and white with a line border for the rest.

## When to use

Every action in app.haysam.school and Haysam websites. One primary button per view; everything else secondary. On posts use `PopButton` or `GlassCTA` instead.

## Markup

```html
<a class="hs-btn hs-btn--primary button-lg" href="...">Plaginni o'rnatish <i class="hs-i hs-i--arrow-down" aria-hidden="true"></i></a>
<button class="hs-btn hs-btn--secondary button-md" type="button"><i class="hs-i hs-i--copy" aria-hidden="true"></i> Nusxalash</button>
```

Always pair `hs-btn` with a size class from the type scale:

| Size | Class | Height | Use |
| --- | --- | --- | --- |
| Large | `button-lg` | 44px | Hero and closing calls to action |
| Medium | `button-md` | 40px | Forms, panels, dialogs |
| Small | `button-sm` | 36px | Nav, toolbars, table rows |
| Extra small | `button-xsm` | 32px | Inside code blocks and dense rows |

- `hs-btn--primary`: `primary` fill, `on-primary` label, `primary-hover` and a 1px lift on hover.
- `hs-btn--secondary`: `surface` fill with an inset `line` border; `background` on hover.
- `hs-btn--done`: success state after copying or saving (`success` label and border); swap the icon to `check` and the label to the past tense.
- `hs-btn--icon`: square icon-only button; give it an `aria-label`.
- `disabled` or `aria-disabled="true"`: half opacity, no lift. (Added for the platform; the site has no disabled buttons.)
- Press: scales to 0.98. Focus: 2px `focus` ring, 2px offset.

## Icons and text links

- Icons are Phosphor Regular at 18px, after the label for direction (`arrow-down`, `arrow-up-right`) and before it for the action (`copy`).
- Inline text links use `hs-link`: `text` colour, underlined, 3px offset.

## Do and don't

- Label with a verb that says what happens: "Plaginni o'rnatish", "Claude'da ochish", "Nusxalash".
- Don't use pill-shaped, glowing, tilted or mono-font buttons in product UI; those are media styles.
