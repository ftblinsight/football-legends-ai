# File Conventions

This document is the source of truth for storing, naming and versioning files in Football Legends AI.

## Repository model

- `library/` contains one canonical copy of reusable source assets.
- `projects/` contains project-specific scripts, storyboards, generations, edits and rights records.
- `references/` inside a project contains symlinks to reusable assets in `library/`.
- `shared/` contains reusable workflows, templates, fonts and brand resources.
- `channel/` contains publishing material for the social channel.

## Naming

Use lowercase, hyphens and no spaces.

```text
person-haaland-2022-23-face-front-001.jpg
team-milan-2005-06-kit-home-001.jpg
stadium-night-floodlights-001.jpg
audio-crowd-stadium-wide-001.wav
shot-s09-shevchenko-goal-v01.mp4
```

Use `v01`, `v02`, `v03` for meaningful revisions. Do not use names such as `final-final.mp4`.

## Git policy

Track scripts, shotlists, prompts, CSV registers, notes, small previews and workflow documentation. Do not track large source videos, Resolve caches, proxies, temporary exports or full AI-generation output. Keep those on the external SSD and back them up separately.

## Asset records

Register external assets in the relevant `source-register.csv` with source, creator, date found, license, analysis/production status and commercial-use status.

## Project workflow

1. Record the decision in `project/decisions/`.
2. Add or update the shotlist.
3. Store prompts in `generation/prompts/`.
4. Store approved inputs and generated outputs in the project folders.
5. Keep rejected generations in `generation/rejected/` until the project is complete.
6. Commit one logical change at a time with a descriptive message.
