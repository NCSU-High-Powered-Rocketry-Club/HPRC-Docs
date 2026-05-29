# HPRC Docs

This repo is for our team related documentation. It uses Zensical. You will need Python with uv to work on this (install uv here: https://docs.astral.sh/uv/getting-started/installation/).

You can view docs online at https://docs.ncsurocketry.org/.

## Getting Started

The docs live under the top-level `docs/` folder and are built using **[Zensical](https://zensical.org/)** and managed through **[uv](https://docs.astral.sh/uv/)**.

### Install the Python dependencies

```bash
uv sync
```

### Run the docs locally

```bash
uv run zensical serve
```

This launches a local dev server (http://127.0.0.1:8000/) where your changes auto-reload as you edit markdown files.

---

To publish changes to the docs, create a PR and merge it to `main`. When creating a PR, the bot will comment a link to view a preview of the docs with your changes. After merging, the docs will be live at [https://docs.ncsurocketry.org/](https://docs.ncsurocketry.org/).
