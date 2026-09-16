# Sumin Jung — Academic Website

[![Website](https://img.shields.io/badge/Website-jasmine00716.github.io-2563eb?style=flat-square)](https://jasmine00716.github.io)
[![Jekyll build](https://github.com/jasmine00716/jasmine00716.github.io/actions/workflows/jekyll-build.yml/badge.svg)](https://github.com/jasmine00716/jasmine00716.github.io/actions/workflows/jekyll-build.yml)

This repository contains the source for my personal academic website. I am a medical AI researcher working on multimodal learning, foundation models, and clinical medical-image analysis, with experience spanning research, software as a medical device, and hospital deployment.

Visit the live site at **[jasmine00716.github.io](https://jasmine00716.github.io)** or view my **[CV (PDF)](https://jasmine00716.github.io/files/SuminJung_CV.pdf)**.

## Site contents

- **[About](https://jasmine00716.github.io/):** research interests, education, industry experience, and selected highlights
- **[Publications](https://jasmine00716.github.io/publications/):** journal articles, conference papers and preprints, presentations, and patents
- **[Research Projects](https://jasmine00716.github.io/portfolio/):** 3D-MoReT, clinical collateral-imaging software, ISLES 2024, PathRadX, and stroke-segmentation research
- **[CV](https://jasmine00716.github.io/cv/):** education, experience, publications, awards, and technical skills
- **[News](https://jasmine00716.github.io/year-archive/):** academic and professional milestones in chronological order

## Research focus

- Large-scale multimodal and foundation models for medical AI
- Vision–language learning and clinical representation learning
- Medical image analysis across MR, CT, and multimodal clinical data
- Efficient 3D deep learning for classification, regression, and segmentation
- Translational AI and software as a medical device

## Repository structure

| Path | Purpose |
| --- | --- |
| `_pages/` | Main pages, including About, Publications, Projects, CV, and News |
| `_publications/` | Individual publication, presentation, preprint, and patent entries |
| `_portfolio/` | Research project descriptions |
| `_posts/` | Dated academic and professional milestones |
| `files/` | Downloadable documents, including `SuminJung_CV.pdf` |
| `images/` | Profile, project, timeline, and site icon assets |
| `_config.yml` | Site metadata, author profile, collections, and Jekyll settings |

## Running locally

The site is built with [Jekyll](https://jekyllrb.com/) and the [Academic Pages](https://academicpages.github.io/) theme.

1. Install Ruby and Bundler.
2. Install the project dependencies:

   ```bash
   bundle install
   ```

3. Start the local server:

   ```bash
   bundle exec jekyll serve -l -H localhost
   ```

4. Open [http://localhost:4000](http://localhost:4000).

Jekyll reloads most Markdown, HTML, and stylesheet changes automatically. After editing `_config.yml`, stop and restart the local server so the new configuration is applied.

### Docker alternative

If Docker is installed, the site can also be run with:

```bash
docker compose up
```

The preview will be available at [http://localhost:4000](http://localhost:4000).

## Updating content

- Add or edit publication records in `_publications/`.
- Add research projects in `_portfolio/`.
- Add milestones in `_posts/` using `YYYY-MM-DD-title.md` filenames.
- Update the web CV in `_pages/cv.md` and replace `files/SuminJung_CV.pdf` when the PDF changes.
- Update personal links and global metadata in `_config.yml`.

Changes pushed to `main` are checked by the repository's Jekyll build workflow and published through GitHub Pages.

## Credits

This site is based on [Academic Pages](https://github.com/academicpages/academicpages.github.io), which is derived from the [Minimal Mistakes](https://github.com/mmistakes/minimal-mistakes) Jekyll theme. See [LICENSE](LICENSE) for licensing information.
