# Resume

[![Build and Deploy Resume](https://github.com/alDuncanson/resume/actions/workflows/resume.yml/badge.svg)](https://github.com/alDuncanson/resume/actions/workflows/resume.yml)

A single-source resume written in Markdown, automatically converted to PDF and HTML.

## Preview

![Resume Preview](https://alduncanson.github.io/resume/preview.png)

[View HTML](https://alduncanson.github.io/resume/) |
[Download PDF](https://alduncanson.github.io/resume/resume.pdf)

## How It Works

The resume is authored in `resume.md` with YAML frontmatter for PDF styling. On every push to `main`, GitHub Actions:

1. Converts the Markdown to PDF using Pandoc with Tectonic as the LaTeX engine
2. Converts the Markdown to standalone HTML
3. Generates a preview image from the PDF
4. Deploys everything to GitHub Pages

## Technologies

- **Pandoc** - Universal document converter for Markdown to PDF/HTML
- **Tectonic** - Modern, self-contained LaTeX engine for PDF generation
- **GitHub Actions** - CI/CD for automated builds and deployment
- **GitHub Pages** - Static hosting for the HTML version

## Local Development

Generate the PDF:

```sh
pandoc resume.md -o resume.pdf --pdf-engine tectonic
```

Generate the HTML:

```sh
pandoc -s resume.md -o resume.html
```
