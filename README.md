# Technical Writing & Documentation Portfolio

Welcome to my Docs-as-Code technical documentation portfolio repository. This project demonstrates end-to-end technical writing capabilities, ranging from developer-focused REST API references to enterprise Standard Operating Procedures (SOPs) and release notes.

**Live Portfolio:** https://cabbagepatchgrl.github.io/tech-docs-portfolio/

---

## Portfolio Navigation & Scope

* **Home (`index.md`)**: Executive summary and portfolio overview.
* **Operations & SOPs (`sop-guide.md`)**: Process workflows and standard operating procedure documentation.
* **GitHub Quickstart (`github-guide.md`)**: Step-by-step onboarding guide for version control workflows.
* **Enterprise Confluence (`confluence-guide.md`)**: Internal knowledge base architecture and documentation standards.
* **Release Notes (`changelog.md`)**: Structured product changelog tracking version updates.
* **API Reference (`api-guide.md`)**: REST API reference including endpoints, authentication headers, cURL examples, and JSON payloads.

---

## Tech Stack & Architecture

This repository uses a modern Docs-as-Code workflow:

* **Markup Language:** Markdown
* **Site Generator:** MkDocs (Material Theme)
* **IDE / Authoring Environment:** Visual Studio Code
* **Version Control:** Git & GitHub
* **CI/CD & Hosting:** GitHub Actions & GitHub Pages

```text
├── docs/
│   ├── assets/                # Image assets, screenshots, and visual figures
│   │   ├── confluence-sop.png
│   │   └── dashboard-overview.png
│   ├── api-guide.md           # REST API Reference & endpoint documentation
│   ├── changelog.md           # Product Release Notes & Changelog
│   ├── confluence-guide.md    # Enterprise Confluence Knowledge Base documentation
│   ├── github-guide.md        # Visual UI guide for GitHub navigation
│   ├── index.md               # Portfolio home page & executive summary
│   └── sop-guide.md           # Standard Operating Procedure (SOP) workflow
├── mkdocs.yml                 # Navigation layout and Material theme configuration
└── README.md                  # Project architecture and local development guide
```

---

## Local Development Setup

To build and preview this site locally on your machine:

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Cabbagepatchgrl/tech-docs-portfolio.git
   cd tech-docs-portfolio
   ```

2. **Install MkDocs Material theme:**
   ```bash
   pip install mkdocs-material
   ```

3. **Start the local development server:**
   ```bash
   mkdocs serve
   ```

4. **View in browser:**
   Open `http://127.0.0.1:8000` to inspect live updates as you edit Markdown files.