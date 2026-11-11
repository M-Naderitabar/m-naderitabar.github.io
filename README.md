# Mohammad Naderitabar — academic website

A personal economics website built on the AcademicPages Jekyll template. The design uses a portrait sidebar, serif headings, and a simple About / Research / Teaching / CV navigation. It works without JavaScript or external font services.

## Updating the website

| What to change | File |
| --- | --- |
| Name, email, affiliation, portrait path, website URL | `_config.yml` |
| Biography | `_pages/about.md` |
| Papers, coauthors, summaries, abstracts, and download links | `_data/research.yml` |
| Teaching experience and optional course materials | `_data/teaching.yml` |
| Education and other CV sections | `_pages/cv.md` |
| Navigation | `_data/navigation.yml` |
| Colors, typography, spacing, and responsive layout | `assets/css/academic.css` |
| Page layout and search/social metadata | `_layouts/academic.html` |

### Update the CV

Replace `files/CV_Mohammad_Naderitabar.pdf` with the updated PDF. Both the sidebar and the CV page link to this file through `cv_pdf` in `_config.yml`. If you rename it, update that setting too.

The CV page also contains a short academic profile. Add degree dates and previous education there when ready.

### Add a paper

Add an entry to `papers` in `_data/research.yml`:

```yaml
  - title: Your paper title
    coauthors:
      - name: First Coauthor
        url: https://example.com/
      - name: Second Coauthor
        url: https://example.org/
    status: Working paper
    summary: >-
      A short description of the research question and contribution.
    abstract: >-
      The full abstract, if you would like an expandable abstract.
    paper_url: /files/your-paper.pdf
    slides_url:
```

Upload the PDF before adding its URL. Full external HTTPS links also work. Coauthor names link to their individual websites. Empty coauthor, abstract, and download fields stay hidden; a missing summary and abstract displays “Description forthcoming.” The first paper is featured on the homepage; all papers appear on the Research page in data-file order. Keep this order when updating individual descriptions.

### Update teaching

Edit `_data/teaching.yml`. Leave `materials_url` empty until you have a real link to share. Add academic years or course descriptions when ready.

### Replace the portrait

Replace `images/profile.jpg` with your preferred photograph, or change `author.avatar` in `_config.yml`. The sidebar crops the image using `object-fit: cover`; adjust `.profile-photo` in the stylesheet if needed.

## Local preview

Install Ruby with its development tools and Bundler, then run:

```sh
bundle install
bundle exec jekyll serve --host 127.0.0.1
```

Open <http://127.0.0.1:4000>. Restart the server after changing `_config.yml`. For a production build:

```sh
JEKYLL_ENV=production bundle exec jekyll build --safe
```

In PowerShell, set the environment first with `$env:JEKYLL_ENV = "production"`, then run `bundle exec jekyll build --safe`.

## GitHub Pages

This checkout is configured for `https://m-naderitabar.github.io`, with an empty `baseurl`. To publish using the standard GitHub Pages Jekyll build, push the changes and select the publishing branch and `/ (root)` under **Settings → Pages → Deploy from a branch**. If Pages is already set up this way, subsequent pushes to that branch rebuild it.

The included **Check Jekyll site** workflow validates builds on pushes and pull requests; it does not deploy. See [GitHub's publishing source documentation](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site).

## Content and template notes

- The biography follows the [existing Google Site](https://sites.google.com/view/m-naderitabar).
- Contact details and teaching experience come from the original checkout. Project titles, order, and linked coauthors follow the user's supplied list and the [Google Site Research page](https://sites.google.com/view/m-naderitabar/research).
- The oil paper is labeled as a working paper, with a paraphrased summary and links to the draft and slides from [Alireza Azampour's website](https://arazampour.com/#jmp). Other project descriptions are placeholders for the author to fill in.
- The CV PDF is the file supplied by the user. Missing dates, degrees, other paper PDFs, and course materials have been left for you to add. There are no invented publication records or inactive download buttons.
- Template demo pages have been removed. Demo collections, PDFs, and tooling are excluded from the built site. Original theme layouts remain available for future extensions. `_data/cv.json` is retained as a minimal personal record; the visible CV uses `_pages/cv.md`.
- Original template: [AcademicPages](https://github.com/academicpages/academicpages.github.io), based on Minimal Mistakes. See `LICENSE` for its license.
