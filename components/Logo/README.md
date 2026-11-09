# Logo

The official Haysam lockup (mark + caps HAYSAM wordmark), placed from the real files and picked by background.

## When to use

On every design that has no photo, and on photo designs as the one place the brand shows. Use the mark alone (`hs-mark--*`) for avatars, app icons, stickers and small spaces.

## Markup

```html
<span class="hs-logo hs-logo--ink" role="img" aria-label="Haysam"></span>
<span class="hs-mark hs-mark--yellow" role="img" aria-label="Haysam"></span>
```

The classes embed the exact SVG files from `assets/Logos` and `assets/Marks`. Height comes from `--logo-height` (52px, right for a 1080px canvas); set it on the element or a parent to resize. Width follows the file's ratio (1416:329).

| Ground | Class |
| --- | --- |
| Lavender, white (default) | `hs-logo--ink` |
| Light ground with the yellow accent | `hs-logo--yellow-ink` |
| `night` (#270601) | `hs-logo--yellow-white` |
| Photos and images | `hs-logo--white` |
| One-colour print | `hs-logo--black` |
| Follows the theme (ink on Lavender, yellow-white on Night) | `hs-logo--auto` |

Wrap it in `hs-logo-clear` to reserve clear space: half the mark's height on every side.

## Do and don't

- Do centre it near the top: about y 330 on a 1080×1920 cover.
- Do keep it at least 32px tall on screen and 20mm wide in print.
- Don't type, redraw, generate, stretch, rotate, recolour, outline or add shadows or effects.
- Don't place it on a busy part of an image or use the retired lowercase "haysam" logo.
