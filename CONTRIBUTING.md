# Editing the UoB AT Lab website

This site is built with [Jekyll](https://jekyllrb.com/) and published automatically
by GitHub Pages every time a change is pushed to the `main` branch. You do **not**
need to install anything or run any build commands — editing the Markdown and front
matter files described below is enough.

All content can be edited directly on GitHub: open a file, click the pencil
(**Edit**) icon, make your change, and click **Commit changes**. Within a minute or
two the live site updates itself.

> **Accessibility note:** every change should keep the site usable with a screen
> reader and keyboard. Always write meaningful link text (not "click here"), give
> every image a descriptive `alt` text, and never skip heading levels.

---

## 1. Add a new project

Each project is a single Markdown file in the [`_projects/`](_projects/) folder.
Adding a file there automatically creates its project page **and** adds a card to
the "Our Projects" list on the homepage — you do not need to edit the homepage by
hand.

### Steps

1. In the `_projects/` folder, create a new file, e.g. `my_project.md`.
   The file name (without `.md`) becomes the page address, so use lowercase
   letters, numbers and underscores only — for example `my_project.md` becomes
   `/projects/my_project.html`.
2. Copy the template below into the file and fill it in.
3. Commit the file. The new card and page appear automatically.

### Template

```markdown
---
layout: project
title: "Full Project Title"
short_title: "Short Title for the Card"   # optional; falls back to title
author: "Author Name"
description: "One-sentence summary shown on the homepage card."
timeline: "Jan 2025 – Apr 2025"           # optional
association: "University of Bristol"       # optional
status: "Active"                           # optional, e.g. Active / Completed
order: 10                                  # optional; lower numbers appear first
repo_url: "https://github.com/org/repo"    # optional button
demo_url: ""                               # optional button (leave "" to hide)
doc_url: ""                                # optional button (leave "" to hide)
---

## Overview
Describe what the project does, who it is for, and why it was created.

## Key Features
* First feature.
* Second feature.

## Installation
Describe how to run the project, if relevant.
```

### Field reference

| Field         | Required | What it does                                                        |
| ------------- | -------- | ------------------------------------------------------------------- |
| `layout`      | yes      | Must be `project`. Leave this exactly as shown.                     |
| `title`       | yes      | Full title, shown at the top of the project page.                   |
| `short_title` | no       | Shorter title for the homepage card. Uses `title` if omitted.       |
| `author`      | no       | Shown on the card and the project page.                             |
| `description` | yes      | One sentence shown on the homepage card. Keep it short.             |
| `timeline`    | no       | Project dates, shown in the page's details box.                     |
| `association` | no       | Affiliation, shown in the page's details box.                       |
| `status`      | no       | e.g. `Active`, `Completed`, shown in the details box.               |
| `order`       | no       | Controls card position on the homepage (lower numbers first).       |
| `repo_url`    | no       | If set, shows a "View Repository" button.                           |
| `demo_url`    | no       | If set, shows a "Live Demo" button. Use `""` to hide it.            |
| `doc_url`     | no       | If set, shows a "Read Documentation" button. Use `""` to hide it.   |

Everything **below** the second `---` is the project page body, written in normal
Markdown (headings, lists, links, code blocks). When you add a fenced code block
with ` ``` `, remember to close it with a matching ` ``` `.

### Card ordering

By default cards are ordered by the optional `order` field (lowest first).
Projects without an `order` value appear first. To pin the order, add an `order`
number to each project (for example `10`, `20`, `30`).

---

## 2. Edit the About section

The text under **About** on the homepage lives in
[`_includes/about.md`](_includes/about.md).

1. Open `_includes/about.md`.
2. Edit the Markdown below the comment block. Do **not** add a heading — the
   "About" heading is added automatically.
3. Commit. The homepage updates itself.

You can use paragraphs, **bold**, _italics_, [links](https://example.com) and
bullet lists.

---

## 3. Edit the Contact section

The text under **Contact** on the homepage lives in
[`_includes/contact.md`](_includes/contact.md).

1. Open `_includes/contact.md`.
2. Edit the Markdown below the comment block. Do **not** add a heading.
3. Commit.

For an email link use `[name@bristol.ac.uk](mailto:name@bristol.ac.uk)`.

---

## 4. Where everything lives

| What you want to change            | File to edit                          |
| ---------------------------------- | ------------------------------------- |
| Add / edit a project               | `_projects/<name>.md`                 |
| About section text                 | `_includes/about.md`                  |
| Contact section text               | `_includes/contact.md`                |
| Navigation links / page shell      | `_layouts/default.html`               |
| Project page layout                | `_layouts/project.html`               |
| Colours, fonts, spacing            | `assets/css/style.css`                |
| Site title / description           | `_config.yml`                         |

---

## 5. Previewing locally (optional)

You only need this if you want to preview before pushing. With
[Ruby and Jekyll installed](https://jekyllrb.com/docs/installation/):

```bash
jekyll serve
```

Then open <http://localhost:4000>. Otherwise, just commit on GitHub and check the
live site after a minute or two.
