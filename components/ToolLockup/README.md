# ToolLockup

The `HAYSAM × [official tool logo] Tool name` line that opens a post about a specific AI tool.

## When to use

At the top of a cover or slide whose subject is one tool, in place of the plain logo.

## What you provide

- The tool's official logo files (Simple Icons, its press kit or site, or Wikimedia Commons): its full-colour or dark version for light grounds, and its white or light version for night covers and photos. Never generate or redraw one. With no official file, leave the image out and keep the name.
- The tool's name as the brand writes it.

## Markup

```html
<span class="hs-lockup">
  <span class="hs-logo hs-logo--ink" role="img" aria-label="Haysam"></span>
  <span class="hs-lockup__x" aria-hidden="true">×</span>
  <img class="hs-lockup__tool" src="google-veo.svg" alt="">
  <span class="hs-lockup__name">Google Veo</span>
</span>
```

Sizes scale from `--logo-height`. The lockup takes its colours from its own ground, never from the page around it:

| Ground | Haysam logo | Tool logo | Name and × |
| --- | --- | --- | --- |
| Lavender or white | `hs-logo--ink` (or `--auto`) | Full-colour or dark version | `ink` (default) |
| Night cover (`hs-night` on the cover) | `hs-logo--yellow-white` (or `--auto`) | White or light version | White, automatically |
| Photo | `hs-logo--white` | White version | White: add `hs-lockup--white` |

## Do and don't

- Keep it on one line, centred near the top.
- One tool per lockup.
- Never a white tool logo or white name on a light ground, or a dark one on night or a photo.
