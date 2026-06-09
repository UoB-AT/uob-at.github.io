# University of Bristol Assistive Technology Lab - Website
This repository contains the source code for the University of Bristol Assistive Technology Lab organization website. It is built using [Jekyll](https://jekyllrb.com/) and hosted via GitHub Pages.

## Architecture
The site is content-driven: research projects and the About/Contact text are defined in Markdown files, and the homepage assembles itself from them. This keeps the markup simple and accessible while letting contributors edit the site without touching HTML.
* **`_projects/`**: One Markdown file per research project. Each file becomes both a project page and a card on the homepage automatically.
* **`_includes/about.md`** and **`_includes/contact.md`**: The editable About and Contact text shown on the homepage.
* **`_layouts/`**: The HTML templates (`default.html` for the shell, `project.html` for individual projects).
* **`assets/css/`**: The WCAG AAA compliant styling (University of Bristol red, Apple/system font).
* **`index.html`**: The homepage. It generates the project list from `_projects/` and renders the About/Contact includes — you should not need to edit it to add content.

## Editing the site
See [CONTRIBUTING.md](CONTRIBUTING.md) for step-by-step instructions on adding a new project and editing the About and Contact sections. In short:
* **Add a project:** create a new `.md` file in `_projects/` using the front matter template — the homepage card and project page appear automatically.
* **Edit About:** edit `_includes/about.md`.
* **Edit Contact:** edit `_includes/contact.md`.

## License
This repository uses a dual-license model:
- The structural software (HTML, CSS, Jekyll configuration) is licensed under the MIT License.
- The academic content (text, research descriptions, imagery) is licensed under the CC BY 4.0 License.
*Please see the LICENSE file for full details.*