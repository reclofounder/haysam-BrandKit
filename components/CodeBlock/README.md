# CodeBlock

A dark, single-line command with a copy button, and inline code inside a sentence.

## When to use

Commands and values people copy: install commands, API keys shown once, invite links. Inline code for short commands mentioned in text.

## Markup

```html
<div class="hs-code"><code class="mono-md">/plugin install haysam-cover@haysam</code><button class="hs-copy button-xsm" type="button">Nusxalash</button></div>
<code class="hs-code-inline mono-xs">/mcp</code>
```

- Block: `code-bg`, `code-text`, `radius-md`, at most 560px wide; long commands scroll sideways inside it.
- Copy button: `code-button`, white `button-xsm` label, `code-button-hover` on hover; after copying add `hs-copy--done` (`success`) and change the label to "Nusxalandi" for two seconds.
- Inline code: `mono-xs` on `background` with a `line` border and `radius-xs`.
- If the clipboard is refused, select the text and show a `danger` caption under the block.
