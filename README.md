# HPRC Docs

This repo is for our team related documentation. It uses Zensical. You will need Python with uv to work on this (install uv here: https://docs.astral.sh/uv/getting-started/installation/).

You can view docs online at https://docs.ncsurocketry.org/.

this is test for splleing mistakesfs HPRC

## Getting Started

The docs live under the top-level `docs/` folder and are built using **[Zensical](https://zensical.org/)** and managed through **[uv](https://docs.astral.sh/uv/)**.

### Install the Python dependencies

```bash
uv sync
```

### Spell check pull requests

The **Spelling** GitHub Actions workflow checks spelling automatically when a pull request is opened, reopened, or updated with new commits. No local installation or GitHub Copilot subscription is needed.

1. Make your documentation changes and push them to your pull request branch.
2. Open the pull request's **Checks** tab and select **spelling** to see any errors and suggested corrections.
3. Fix the reported spelling errors and push another commit. The check runs again and passes when no spelling errors remain.

The check scans entire Markdown (`.md`) files changed in the pull request, including `README.md`, so it can report existing mistakes outside the lines you edited. It checks spelling, not sentence grammar, and does not automatically edit files.

If a correctly spelled technical term, name, or acronym is flagged, add it to the `words` list in [`cspell.json`](cspell.json). Keep existing entries and add the new term as a quoted string separated by a comma. Only add legitimate terms; fix actual typos in the document.

To test the workflow, temporarily add an intentional typo to a Markdown file on your pull request branch and push a commit. Confirm that the spelling check fails and identifies it, then remove the typo and push again. Other unrecognized words in that file must also be corrected or added to the dictionary before the check can pass.

### Run the docs locally

```bash
uv run zensical serve
```

This launches a local dev server (http://127.0.0.1:8000/) where your changes auto-reload as you edit markdown files.

---

To publish changes to the docs, create a PR and merge it to `main`. When creating a PR, the bot will comment a link to view a preview of the docs with your changes. After merging, the docs will be live at [https://docs.ncsurocketry.org/](https://docs.ncsurocketry.org/).
