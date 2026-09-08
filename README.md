# LaVA project page

Source for <https://lava-inference-search.github.io>

Built on the [Academic Project Page Template](https://github.com/eliahuhorwitz/Academic-project-page-template),
which was adapted from the [Nerfies](https://nerfies.github.io) project page.

## Replace before publishing

| Path | Content |
| --- | --- |
| `static/images/image1.jpg` | Figure 1 — the LaVA search step diagram (used twice on the page) |
| `static/images/image2.jpg` | Table 1 — main inference-time scaling results |
| `static/images/image3.jpg` | Figure 2 — OpenL3-FD vs. particle count, per layer |
| `static/images/image4.jpg` | Tables 2 and 3 — verifier objective and head architecture |
| `static/images/favicon.ico` | Site icon (currently referenced but missing) |
| `static/pdfs/lava.pdf` | The paper |
| `static/audio/prompt*.wav` | Audio samples for the Listen section |

Export figures straight from the compiled PDF:

```bash
pdftoppm -jpeg -r 250 -f 1 -l 1 LAVA_fig1.pdf static/images/image1
```

Then search `index.html` for `TODO` — the venue subtitle, arXiv ID, Twitter handles,
one author link, and the two audio prompt captions are all still placeholders.

## Preview locally

```bash
python -m http.server 8000
```

Then open <http://localhost:8000>.
