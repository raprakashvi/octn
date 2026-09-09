# OCTN: Neural OCT Representations for Robot-Guided Precision Intervention

Project website for **OCTN** (pronounced *"octane"*), an implicit neural representation
framework that converts volumetric OCT scans into a continuous, differentiable, and
spatially faithful tissue-intensity field.

🌐 **Website:** [raprakashvi.github.io/octn](https://raprakashvi.github.io/octn/)
📄 **Paper:** [arXiv:2609.06810](https://arxiv.org/abs/2609.06810)
🎥 **Video:** [YouTube](https://youtu.be/riD9-W3JwzE)

**Authors:** Ravi Prakash, Ryan P. McNabb, Patrick J. Codd, Shan Lin
Duke University • Arizona State University

## Local Preview

```bash
python3 -m http.server 8000
```

Then open <http://localhost:8000>.

> The site loads `data/paper.json` via `fetch()`, so it must be served over HTTP —
> opening `index.html` directly from the filesystem will not work.

## Editing Content

Nearly all content lives in **`data/paper.json`**: title, abstract, authors, buttons,
tags, figures, video ID, institution logos, and BibTeX.

Note that `paper.json` must be **strict JSON** — no trailing commas and no `//` comments.
If the file fails to parse, the page renders blank. Validate before committing:

```bash
python3 -c "import json; json.load(open('data/paper.json'))"
```

Figures referenced from `galleryFigures` must be web-renderable raster images
(PNG/JPG). Browsers cannot display a PDF inside an `<img>` tag, so export or convert
vector figures first:

```bash
pdftoppm -png -r 200 -singlefile figure.pdf figure
```

## Layout

- `index.html` — page structure and social/meta tags
- `data/paper.json` — all content
- `data/OCTN.pdf` — hosted copy of the paper
- `assets/css/style.css` — styling
- `assets/js/main.js` — renders `paper.json` into the page
- `assets/img/figures/` — paper figures
- `assets/authors/` — author photos
- `assets/img/logo/` — institution logos

## Citation

```bibtex
@misc{prakash2026octn,
  title         = {OCTN: Neural OCT Representations for Robot-Guided Precision Intervention},
  author        = {Prakash, Ravi and McNabb, Ryan P. and Codd, Patrick J. and Lin, Shan},
  year          = {2026},
  eprint        = {2609.06810},
  archivePrefix = {arXiv},
  primaryClass  = {cs.RO},
  doi           = {10.48550/arXiv.2609.06810},
  url           = {https://arxiv.org/abs/2609.06810}
}
```

---

Website template by **Ravi Prakash** — [raprakashvi.github.io](https://raprakashvi.github.io/)
