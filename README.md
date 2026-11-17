# justinhawkes.dev

Source for my portfolio site, live at **[justinhawkes.dev](https://justinhawkes.dev)**.

One hand-written `index.html`. No framework, no build step, no dependencies to
install — open the file in a browser and you are looking at the real site. Every
style and script is inline, so there is exactly one place to look when something
renders wrong.

That is a deliberate choice rather than a shortcut. A personal site is edited a few
times a year, usually in a hurry; a toolchain that needs `npm install` before a
one-line copy fix is a tax that gets paid at the worst moment. The whole site is
about 300 KB, most of it a portrait and an OG image.

## What's here

| Path                     | What it is                                                                                      |
| ------------------------ | ----------------------------------------------------------------------------------------------- |
| `index.html`             | The entire site — markup, styles, and scripts in one file                                       |
| `more.html`, `more/`      | The second page, "More I've built": side projects, with its one image                         |
| `maps/*.svg`             | Architecture diagrams for Atlas, Nova, RepoLens, Revline, and JobFitr, opened in a modal viewer |
| `portrait.jpg`, `og.png` | Portrait, and the social-preview card                                                           |
| `CNAME`                  | Points GitHub Pages at the custom domain                                                        |
| `.nojekyll`              | Stops Pages from running Jekyll over the files                                                  |

## Running it

```bash
open index.html            # macOS — that's it
python3 -m http.server     # if you need real URLs, e.g. to test the OG card
```

## Deploying

Push to `main`. GitHub Pages serves the repository root, `CNAME` maps it to
justinhawkes.dev, and there is no build to wait on.

## Two details worth knowing before editing

**The page can hand itself to an AI.** A "copy as AI context" control serialises
the page to Markdown so it can be pasted into an assistant. If you restructure the
markup, check that path still produces something readable — it reads the DOM, so it
breaks silently rather than loudly.

**Analytics is [GoatCounter](https://www.goatcounter.com/)** — no cookies, no
cross-site tracking, and the only third-party request on the page.

## License

**Code is MIT. The personal content is not.** The markup, styles, and scripts are
free to reuse. The portrait, the written copy, and the architecture diagrams are
mine and are not licensed for reuse — a portfolio is an identity document, and a
permissive licence on someone's face and biography is not a thing I want to grant
by accident. See [LICENSE](LICENSE) for the exact split.
