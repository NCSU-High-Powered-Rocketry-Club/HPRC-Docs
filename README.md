# HPRC Docs

This repo is for our team related documentation. It uses Material for MkDocs. You will need Python with uv to work on this (install uv here: https://docs.astral.sh/uv/getting-started/installation/).

## Getting Started

The docs live under the top-level `docs/` folder and are built using **MkDocs + Material** and managed through **uv**.

### Install the Python dependencies

```bash
uv sync
```

### Run the docs locally

```bash
uv run mkdocs serve
```

This launches a local dev server (http://127.0.0.1:8000/docs/) where your changes auto-reload as you edit markdown files.

---

To publish changes to the docs, create a PR and merge it to `main`. Then you can view it at