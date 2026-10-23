# Instructions for Codex

## Project at a glance

The Dial-Up Chronicles (Persian title: خاطراتِ اتصال) is a calm, reflective documentary podcast about the human history of the web, told through personal memories from Zabol and the perspective of an independent engineer.

The project rule is: **planning should make production easier, not heavier.** Keep notes short, use the existing episode checklist as the single task tracker, and create extra documents only when they help make or publish an episode.

## Follow these project decisions

- Shared project documentation and filenames are in English. Podcast scripts are separate Markdown files under each episode's `languages/fa/` and `languages/en/` folders.
- Persian is the source language for writing. Once it is stable, adapt it into natural spoken English; do not translate word for word.
- The pilot is a test of both language versions. Publish them in separate YouTube podcast playlists, with separate narration and edits. Reuse suitable visuals where practical.
- Episodes end with a short final reflection, a one-sentence preview of the next episode, and a brief invitation to contribute. Aim for about 30 seconds total; keep it natural.
- For manual YouTube video uploads, RSS is not needed.
- The public GitHub Pages site is built from Markdown in `docs/`. Assume any file included in `docs/` can be read by the public. Keep credentials, private information, unlicensed media, raw recordings, and large exports out of the repository.
- Never claim that a remembered detail is verified history. Preserve source links and distinguish recollection, interpretation, and researched facts.

## When creating an episode

1. Check the roadmap and existing episode IDs; use the next available three-digit ID and a short folder slug.
2. Copy `docs/episodes/_template/` into `docs/episodes/NNN-short-title/`. Do not edit the template to create the new episode.
3. Fill only what is useful: the brief, Persian source script, English adaptation, checklist, and any research/audio/visual notes actually needed. Keep language versions in their separate folders.
4. Give the episode a clear next action in its checklist. Avoid creating duplicate task trackers.
5. Add the relevant episode pages to `nav` in `mkdocs.yml`, grouping them under Episodes and the correct episode. Link both scripts separately. Do not expose the starter template in site navigation.
6. Add the contribution guide link to the video description checklist. Record each language's publication date and URL separately in the episode brief.

Do not invent personal memories, dialogue, release dates, episode facts, or the next episode topic. Leave an obvious placeholder or ask a focused question when the missing detail affects the work. Continue with independent parts of the task.

## Editing and checking

- Read the relevant existing file and its nearby project guidance before editing.
- Keep public project documentation in English; keep episode script content in its declared language.
- Prefer Markdown and edit the source files in place. Do not edit generated `site/` output.
- Keep task lists concise and actionable. Update the existing episode checklist rather than adding another tracker.
- For documentation/site changes, run `python -m mkdocs build --strict` and fix build warnings or broken internal links.
- Do not add dependencies, media, or elaborate tooling unless needed for the requested task.
- Summarize what changed, how it was checked, and any unresolved content decisions.

## Commits, pushes, and external publishing

- Make edits and prepare a reviewable result first. Never commit, push, open a pull request, publish a website/video, or send a message unless the user asks for that action.
- When the user explicitly asks Codex to commit and push, check the diff and repository status, stage only the intended project changes, use a short descriptive commit message, and push to the requested branch or fork. Report the commit and push result.
- For community contributions, work on the contributor's fork/branch and open a pull request for review; do not push a contribution directly to the project default branch.
- A local Git commit is not the same as publishing an episode to YouTube. Treat YouTube publication as a separate action that requires an explicit request and the necessary account access.
- Before a public release, confirm the user has approved the final scripts, captions, artwork, and audio rights. The site and repository may reveal drafts, research notes, and prompts.

## Repository map

- `docs/project-charter.md`: mission, audience, format, and project decisions.
- `docs/production-workflow.md`: lightweight episode process and outro format.
- `docs/planning/`: roadmap, series arc, backlog, and release calendar.
- `docs/episodes/_template/`: copyable episode starter.
- `docs/episodes/`: episode briefs, separate language scripts, checklists, and optional production notes.
- `docs/decisions/`: durable decisions and their rationale.
- `docs/assets/` and `docs/prompts/`: asset records and versioned generation prompts.
- `docs/contributing.md`: contributor workflow using GitHub Desktop and Codex.
- `mkdocs.yml`: site navigation and build configuration.
- `README.md`: repository entry point and local/site instructions.
