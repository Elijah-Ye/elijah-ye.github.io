# Elijah Gaohan Ye - Personal Website

Personal academic website built with [Jekyll](https://jekyllrb.com/) using the [al-folio](https://github.com/alshedivat/al-folio) theme.

**Live Site:** [https://elijah-ye.github.io](https://elijah-ye.github.io)

## About

This website showcases my academic work, research publications, projects, and professional experience in computer architecture and hardware design. I am a Master's student at the University of Illinois Urbana-Champaign specializing in Electrical and Computer Engineering with a focus on hardware-software co-design for Large Language Model acceleration.

## Features

- **Publications:** Automatically generated from BibTeX bibliography
- **Projects:** Portfolio showcasing technical projects (RISC-V processor, FPGA designs, etc.)
- **Blog:** Technical blog with support for math typesetting and code highlighting
- **CV/Resume:** Generated from JSON Resume format
- **News/Announcements:** Recent updates and achievements
- **Dark Mode:** Toggle between light and dark themes
- **Responsive Design:** Mobile-friendly layout

## Table of Contents

- [Local Development Setup](#local-development-setup)
- [Site Structure](#site-structure)
- [Customization](#customization)
- [Deployment](#deployment)
- [License](#license)

## Local Development Setup

### Prerequisites

Ensure you have the following installed on your system:
- [Ruby](https://www.ruby-lang.org/en/downloads/) (for managing Ruby gems, consider using [rbenv](https://github.com/rbenv/rbenv))
- [Bundler](https://bundler.io/)
- [Python](https://www.python.org/) and [pip](https://pypi.org/project/pip/)

### Running Locally

1. Clone the repository (if you haven't already):
```bash
git clone https://github.com/Elijah-Ye/Elijah-Ye.github.io.git
cd Elijah-Ye.github.io
```

2. Install Ruby dependencies:
```bash
bundle install
```

3. Install Jupyter (if needed for blog posts):
```bash
pip install jupyter
```

4. Serve the site locally:
```bash
bundle exec jekyll serve --lsi
```

5. Open your browser and navigate to `http://localhost:4000`

The site will automatically reload when you make changes to the source files.

## Site Structure

```
├── _bibliography/        # BibTeX files for publications
│   └── papers.bib       # Research publications
├── _config.yml          # Main site configuration
├── _data/               # Data files (coauthors, repositories)
├── _news/               # News and announcements
├── _pages/              # Main site pages
│   ├── about.md        # Homepage/About page
│   ├── cv.md           # CV page
│   ├── projects.md     # Projects portfolio
│   ├── publications.md # Publications page
│   └── blog.md         # Blog listing
├── _posts/              # Blog posts
├── _projects/           # Individual project pages
├── assets/
│   ├── img/            # Images
│   ├── pdf/            # PDF files (papers, CV)
│   └── json/           # JSON data (resume.json)
└── _site/               # Generated site (don't edit)
```

## Customization

### Key Configuration Files

- **`_config.yml`** - Main site settings (name, email, social links, features)
- **`assets/json/resume.json`** - Structured CV/resume data following [JSON Resume](https://jsonresume.org/) standard
- **`_bibliography/papers.bib`** - Publications in BibTeX format
- **`_pages/about.md`** - Homepage content

### Adding Content

**Publications:** Edit `_bibliography/papers.bib` and add new BibTeX entries. Mark papers with `selected={true}` to feature them on the homepage.

**Projects:** Create a new markdown file in `_projects/` directory with frontmatter including title, description, image, and category.

**Blog Posts:** Add markdown files to `_posts/` following the naming convention `YYYY-MM-DD-title.md`.

**News Items:** Add short announcements to `_news/` directory.

## Deployment

The site is automatically deployed to GitHub Pages via GitHub Actions whenever changes are pushed to the `master` branch. The deployment workflow builds the site and publishes it to the `gh-pages` branch.

**Live URL:** [https://elijah-ye.github.io](https://elijah-ye.github.io)

## Technologies Used

- **Jekyll** - Static site generator
- **al-folio** - Academic theme
- **GitHub Pages** - Hosting
- **BibTeX** - Publication management
- **JSON Resume** - Structured CV data
- **MathJax** - Math typesetting
- **Bootstrap** - Responsive design

## Acknowledgments

This website is built using the [al-folio](https://github.com/alshedivat/al-folio) theme, a beautiful academic theme for Jekyll.

## License

This project is licensed under the MIT License. The al-folio theme is also available as open source under the terms of the [MIT License](https://github.com/alshedivat/al-folio/blob/master/LICENSE).
