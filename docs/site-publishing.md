# Site publishing

The public site is built from Markdown files in `docs/` using MkDocs. This is MkDocs' standard source directory, so episode scripts, project plans, prompts, and production notes render as pages without maintaining duplicate copies. Navigation is generated from the Markdown tree; copying the episode template creates pages automatically.

## Preview locally

Install the pinned dependencies and start the live preview:

```powershell
python -m pip install -r requirements.txt
python -m mkdocs serve
```

Open the local address printed by MkDocs. Changes to Markdown files appear in the preview as you edit.

## Build locally

```powershell
python -m mkdocs build
```

The generated site is written to `site/`, which is ignored by Git.

## Publish with GitHub Pages

The workflow in `.github/workflows/publish-site.yml` builds and deploys the site when changes are pushed to `main` or `master`, and can also be run manually. In the repository's GitHub Pages settings, set **Build and deployment → Source** to **GitHub Actions**.

The repository must exist on GitHub and Pages must be available for it. The live URL is set as `site_url` in `mkdocs.yml`, which lets MkDocs generate the correct canonical links for this project site.

## Public content

Every included Markdown page is public when the Pages site is public. Draft scripts, research notes, prompt records, and planning pages are included by design. Keep private information, unpublished details that should remain confidential, credentials, and uncleared media out of the published source. The starter template and contributor guide are excluded from the site.
