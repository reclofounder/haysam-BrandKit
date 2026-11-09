# Tabs

A segmented tab bar: a tinted, bordered track with the selected tab raised in white.

## When to use

Switching between two to four parallel views of the same content (installation for Claude Code or claude.ai, monthly or yearly prices). Not for navigation between pages.

## Markup

```html
<div class="hs-tabs" role="tablist" aria-label="Qayerga o'rnatasiz">
  <button class="hs-tab button-sm" role="tab" aria-selected="true" aria-controls="panel-code">Claude Code va Desktop</button>
  <button class="hs-tab button-sm" role="tab" aria-selected="false" aria-controls="panel-web" tabindex="-1">claude.ai</button>
</div>
```

- Track: `background` fill, `line` border, `radius-md`, 4px padding and gap.
- Tab: `text-muted`, `radius-sm`; hover `text`; selected `surface` with `shadow-xs`.
- Below 720px the bar fills the width and tabs share it equally.
- You provide the panels and the script that sets `aria-selected`, `tabindex` and shows the matching panel.
