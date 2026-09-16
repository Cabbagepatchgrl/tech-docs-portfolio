# Technical Documentation & Knowledge Base Portfolio

A public, production-ready technical writing portfolio built with a **Docs-as-Code** workflow (Markdown, VS Code, Git, MkDocs, GitHub Pages) and integrated with **Enterprise Knowledge Management** standards (Atlassian Confluence).

**Live Portfolio Site:** [https://cabbagepatchgrl.github.io/tech-docs-portfolio/](https://cabbagepatchgrl.github.io/tech-docs-portfolio/)

---

## 🛠️ Architecture & Tech Stack

* **Documentation Generator:** [MkDocs](https://www.mkdocs.org/) with the [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/) theme.
* **Content & Markup:** Clean, structured Markdown (`.md`) formatted for web accessibility and scannability.
* **Version Control & CI/CD:** Git, GitHub repository, and automated deployment via GitHub Pages (`gh-deploy`).
* **Enterprise Tooling:** Atlassian Confluence workspace integration featuring dynamic macros (status tags, callouts, and structured knowledge hubs).

---

## 📁 Repository Structure

```text
tech-docs-portfolio/
├── docs/
│   ├── assets/                # Image assets, screenshots, and visual figures
│   │   ├── confluence-sop.png
│   │   └── dashboard-overview.png
│   ├── changelog.md           # Product Release Notes & Changelog
│   ├── confluence-guide.md    # Enterprise Confluence Knowledge Base documentation
│   ├── github-guide.md        # Visual UI guide for GitHub navigation
│   ├── index.md               # Portfolio home page & executive summary
│   └── sop-guide.md           # Standard Operating Procedure (SOP) workflow
├── mkdocs.yml                 # Navigation layout and Material theme configuration
└── README.md                  # Project architecture and local development guide
