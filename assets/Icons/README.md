# Icons

Phosphor Icons, Regular weight, version 2.1.1 (MIT, `LICENSE-phosphor.txt`): the icons haysam-cover.vercel.app uses. 256×256 SVG with `fill="currentColor"`.

| File | Use |
| --- | --- |
| `arrow-down.svg` | Install and download buttons |
| `arrow-up.svg` | Back to top, upload |
| `arrow-up-right.svg` | Opens in another app or site |
| `copy.svg` | Copy buttons |
| `check.svg` | Done state after copying or saving |
| `download-simple.svg` | Download a file |
| `lightbulb.svg`, `shuffle.svg`, `seal-check.svg`, `plugs-connected.svg`, `puzzle-piece.svg` | Feature icons in icon tiles; `puzzle-piece` in the "Claude uchun plagin" eyebrow |

In HTML use `<i class="hs-i hs-i--copy" aria-hidden="true"></i>`: it draws in the current text colour. Shown as an image, the files render black, so in icon tiles use the class with `ink`. Size: 18px in buttons, 24px in a 40px icon tile. Add more icons from the same set and weight (phosphoricons.com), then run `node scripts/build.mjs`.
