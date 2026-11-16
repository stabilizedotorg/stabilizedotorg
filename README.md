# stabilize.org

The website for [Stabilize.org](https://stabilize.org/), which is building field infrastructure for Earth systems stabilization. Stabilize.org is part of ARC at Renaissance Philanthropy.

This first version is a single landing page.

## What is here

| Path | What it is |
| --- | --- |
| `index.html` | The page: hand-written HTML with its CSS and a short script inline. There is no build step. |
| `img/` | The hero photographs, the cut-outs that sit in front of the dashed line, and the link-preview image. |
| `fonts/` | Hepta Slab Light and Zalando Sans Regular, with their licenses. |
| `logos/` | The Stabilize.org wordmark. |
| `favicon.ico` | The site icon. |
| `robots.txt`, `sitemap.xml` | For search engines. |
| `CREDITS.md` | Who made each photograph and font, and under what terms. |

## Preview it

Any static file server will do. From this folder:

```bash
python3 -m http.server 8000
```

Then open <http://localhost:8000/>.

The hero shows a different photograph on each load. Add `?photo=reef`, `?photo=sea-ice`, `?photo=bison`, or `?photo=amazon` to the address to see a particular one.

## How the page works

- **One photograph, one band.** The photograph fills the screen and a plum band at its foot carries the headline.
- **The dashed line.** It runs along the photograph's top and sides and around the footer. In each photograph one subject sits in front of it: the reef's purple coral, two ice floes, the bison's hump, the river. Each of those is a cut-out of the photograph itself (`img/*-2000.webp`), laid exactly over it.
- **No outside requests.** Fonts and images are served from this repository.
- **Motion** is CSS only and is switched off for visitors who ask for reduced motion.

## License

The code in this repository is released under the [MIT License](LICENSE). The photographs, fonts, logos, and icon are not covered by it and keep their own terms; see [CREDITS.md](CREDITS.md).
