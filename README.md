# The Dial-Up Chronicles | خاطراتِ اتصال

A Persian-first documentary podcast about the human history of the web, told through personal memory, research, and reflection.

The project follows one practical rule: **planning should make production easier, not heavier**. Keep notes concise, use the episode template, and add detail only when it helps make or publish an episode.

## Podcast site

The Markdown source is published as a website with MkDocs and GitHub Pages: [open the live podcast site](https://soroush-zendedel.github.io/The-Dial-Up-Chronicles/).

- Site home source: [docs/index.md](docs/index.md)
- Local preview and publishing guide: [docs/site-publishing.md](docs/site-publishing.md)
- Contribution guide: [docs/contributing.md](docs/contributing.md)

## Project structure

All authored project content lives under `docs/` so MkDocs can render it directly. There is one source file for each piece of content; the site does not maintain duplicate copies.

```text
docs/
├── index.md                         # Podcast site home
├── project-charter.md               # Mission, format, audience, pilot premise
├── editorial-guidelines.md          # Storytelling and fact-checking guardrails
├── production-workflow.md            # Lightweight episode workflow
├── audio-rights-policy.md            # Audio source and rights records
├── site-publishing.md                # Local preview and GitHub Pages
├── decisions/                        # Short records of lasting project choices
├── planning/                         # Roadmap, backlog, release calendar, series arc
├── episodes/
│   ├── _template/                    # Copy to start an episode; not published
│   └── 001-first-connection/         # Pilot brief, scripts, research, production notes
├── assets/                           # Cleared brand, music, and sound records/assets
└── prompts/                          # Versioned music, sound, and cover prompts
```

Persian is the source language for writing. Once it is stable, adapt it into natural spoken English. Keep each language's script, recording, and video edit separate; publish language versions in separate YouTube podcast playlists. The pilot will test both languages before a regular English schedule is decided. Episode files remain under `languages/fa/` and `languages/en/`. The episode checklist is the single detailed status tracker.

## Work on the site locally

```powershell
python -m pip install -r requirements.txt
python -m mkdocs serve
```

To build the static site into `site/`:

```powershell
python -m mkdocs build
```

## GitHub Pages

The workflow at `.github/workflows/publish-site.yml` builds and deploys the site on pushes to `main` or `master`. In repository settings, select **Settings → Pages → Build and deployment → GitHub Actions** as the publishing source.

## Languages and public content

Shared project documentation and filenames are in English. Episode scripts are stored separately in Persian and English. Pages included in the site are public when the site is public, including drafts, research notes, prompts, and planning pages. Keep confidential details, credentials, and uncleared media out of the published source.

Only use audio or images when their source and rights are clear. Approved, practical-size assets can be stored under `docs/assets/`; keep bulky raw recordings and exports in approved external storage.
