# University of Bristol Assistive Technology Lab - Website
This repository contains the source code for the University of Bristol Assistive Technology Lab organization website. It is built using [Jekyll](https://jekyllrb.com/) and hosted via GitHub Pages.

## Architecture
The site uses a static, hardcoded architecture to ensure absolute control over the DOM structure, prioritizing screen reader accessibility and clear structural boundaries.
* **`_projects/`**: Contains the Markdown files for each individual research project.
* **`_layouts/`**: Contains the HTML templates (`default.html` for the shell, `project.html` for individual projects).
* **`assets/css/`**: Contains the WCAG AAA compliant styling.
* **`index.html`**: The static homepage containing manually defined lists for maximum structural control.

## Adding new projects
1. Create the Project Page: Create a new `.md` file inside the `projects/` directory using the existing YAML front matter structure
2. Update the Homepage: Open `index.html` and manually add a new `<li>` element inside the `<ul class="project-list"> section to ensure the new project is linked and accessible from the root domain. 

## License
This repository uses a dual-license model:
- The structural software (HTML, CSS, Jekyll configuration) is licensed under the MIT License.
- The academic content (text, research descriptions, imagery) is licensed under the CC BY 4.0 License.
*Please see the LICENSE file for full details.*