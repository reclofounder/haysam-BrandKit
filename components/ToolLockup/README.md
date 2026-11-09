# ToolLockup

The `HAYSAM × [official tool logo] Tool name` line that opens a post about a specific AI tool.

## When to use

At the top of a cover or slide whose subject is one tool, in place of the plain logo.

## What you provide

- The tool's official logo file (Simple Icons, its press kit or site, or Wikimedia Commons). Never generate or redraw one. With no official file, leave the image out and keep the name.
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

Sizes scale from `--logo-height`. On `night`, use `hs-logo--yellow-white` or `hs-logo--auto`; the name takes the `text` colour.

## Do and don't

- Keep it on one line, centred near the top.
- One tool per lockup.
