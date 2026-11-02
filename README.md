# sreevatsankk.github.io

Personal website of **Sreevatsank Kadaveru**, Ph.D. student at UC San Diego (WCSNG lab), building networks and systems for Physical AI.

Built with Jekyll on the [AcademicPages](https://github.com/academicpages/academicpages.github.io) template and deployed to GitHub Pages with GitHub Actions.

## Where things live

| What | File(s) |
| --- | --- |
| Name, sidebar bio, email, Google Scholar / ORCID / GitHub / LinkedIn | `_config.yml` (`author:`) |
| Homepage: intro, internship callout, research overview | `_pages/about.html` |
| Homepage news timeline | `_data/news.yml` |
| Research projects | `_research/*.md`, with sections defined in `_data/research_groups.yml` |
| Publications | `_publications/*.md` |
| CV page | `_pages/cv.html`, which mirrors the wording and structure of the resume |
| CV PDF and hosted reports, proposals, and posters | `files/` (`cv_pdf` in `_config.yml` names the CV and adds the "Download PDF CV" button) |
| Search engine data about you (roles, schools, topics, awards) | `_data/profile.yml` |
| Top navigation | `_data/navigation.yml` |
| Profile photo, figures, favicons, social preview | `images/` |
| Site-specific styles | `_sass/layout/_custom.scss` |

### Add a news item

Add an entry to the top of `_data/news.yml`. `date: 2026-11` shows the month; a bare year leaves it out. `text` is Markdown.

```yaml
- date: 2026-11
  text: "Gave a talk on **mmsRAN** at ..."
```

### Add a publication

Create `_publications/YYYY-MM-DD-short-name.md`. `category` is one of the keys under `publication_category` in `_config.yml`. Your name is bolded in the author list automatically.

```yaml
---
title: "Paper title"
category: conferences          # or: short
type: Demo                     # optional tag, e.g. Demo, Poster, Work-in-Progress
date: 2027-05-01
venue: "ACM SIGCOMM 2027"
location: "City, Country"
authors: ["Sreevatsank Kadaveru", "Co-author", "Dinesh Bharadia"]
selected: true                 # also list it on the homepage
paperurl: "https://doi.org/..."
project: name                  # optional: the project in _research/name.md, which then lists this paper
doi: "10.1145/..."             # optional: used in the citation data
pdfurl: "https://..."          # optional: a public PDF, used in the citation data
links:
  - label: Code
    url: https://github.com/...
bibtex: |
  @inproceedings{...}
---
```

### Add a research project

Create `_research/name.md`. `group` picks the section on the Research page and `order` sorts projects within it. Figures go in `images/research/`; set `image_size: [width, height]` so the page can reserve their space. Use `figure: wide` for very wide figures, which are shown above the text instead of beside it. The Markdown body is the description. Sections marked `compact` in `_data/research_groups.yml` show half-width boxes, and those also marked `expandable` need a two- or three-sentence `teaser`, an abstract that always shows and that also opens the project's page. The rest of the description appears when the box is selected.

Each project also gets its own page at `/research/name/`, so it needs its own `seo_title` (at most 60 characters) and `description` (110 to 160 characters) for search results.

```yaml
---
title: "Project: Subtitle"
seo_title: "Project: Short Subtitle | Sreevatsank Kadaveru"
description: "One or two sentences that appear under the page's title in search results."
group: physical-ai
order: 5
period: "2026 – present"
image: /images/research/project.png
image_size: [1500, 900]
image_alt: "What the figure shows"
badges: ["NSDI 2027"]
team: "with ..."
links:
  - label: Paper
    url: https://...
---
One paragraph about the project.
```

Link labels choose their icon automatically. The recognized labels are Paper, PDF, Project Page, Poster, Proposal, Slides, Code, Demo, Video, arXiv, and Report, and any label ending in "Page" or containing "Website". Put documents in `files/` and link them as `/files/name.pdf` rather than hosting them elsewhere. Never add slide decks.

## Preview locally

You need Ruby with Bundler, and Node.js for minifying the JavaScript.

```bash
bundle install
npm install && npm run build:js     # builds assets/js/main.min.js
bundle exec jekyll serve -l -H localhost
```

Then open <http://localhost:4000>. Changes to `_config.yml` need a server restart.

If you would rather not install Ruby, the template's `Dockerfile`, `docker-compose.yaml`, and `.devcontainer/` set up the same environment in a container.

## Deploy

1. Create a public GitHub repository named `sreevatsankk.github.io` and push this folder to its `main` branch.
2. In the repository, go to **Settings → Pages** and set **Source** to **GitHub Actions**.
3. Every push to `main` then runs `.github/workflows/jekyll.yml`, which builds the site and publishes it at <https://sreevatsankk.github.io>.

## Credits

The site template is [AcademicPages](https://github.com/academicpages/academicpages.github.io), a fork of [Minimal Mistakes](https://mademistakes.com/work/minimal-mistakes-jekyll-theme/), released under the MIT License (see `LICENSE`). The site content, including text, photos, and research figures, is © Sreevatsank Kadaveru and co-authors.
