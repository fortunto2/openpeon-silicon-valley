# Silicon Valley Sound Pack — CLAUDE.md

## What this repo is

A CESP 1.0 sound pack for [peon-ping](https://github.com/PeonPing/peon-ping) with quotes from Silicon Valley. Russian dub by «Кубик в кубике».

## Key files

- `openpeon.json` — the manifest. All category assignments, sound metadata, version, sha256 hashes.
- `sounds/` — 59 mp3 files. Some sounds appear in multiple categories (duplicates are intentional).
- `README.md` — user-facing docs with install instructions and category philosophy.

## Category assignment rules

When adding or moving sounds between categories, follow this philosophy:

| Category | Intent | What goes here |
|---|---|---|
| `session.start` | **Biggest category.** Energetic, expressive, memorable. | Swearing, exclamations, iconic one-liners. This is the "hello" moment — make it loud and fun. Move expressive lines here from other categories. |
| `task.complete` | Celebration, satisfaction. | "Done!", triumphant lines. |
| `task.acknowledge` | Calm confirmations. | "I like it", "Вот именно". Low-energy acknowledgements. |
| `task.error` | **Keep minimal.** Genuine "something broke" reactions only. | "Проекту конец", "Ну вот опять". NO expressive swearing — move those to `session.start`. |
| `input.required` | Attention-grabbers, "hey look at this". | Jian Yang lines, "В душе не ебу". |
| `resource.limit` | Despair, running out of resources. | "Not the doors of a billionaire", "Невезуха заразна". |
| `user.spam` | **Keep minimal.** Actual annoyance at repeated prompts. | "Говнюк", "Ты чё творишь". Move energetic swearing to `session.start` instead. |

**Key principle:** When in doubt, put expressive/funny/sweary lines in `session.start`. Keep `task.error` and `user.spam` small.

## Duplicates

Sounds can appear in multiple categories. This is intentional — a good line for `session.start` might also work in `task.complete`.

## Versioning

- Version lives in `openpeon.json` → `"version"` field.
- Tag each release: `git tag vX.Y.Z && git push origin vX.Y.Z`
- After pushing, update the entry in [PeonPing/registry](https://github.com/PeonPing/registry) `index.json`:
  - Update `version`, `source_ref`, `manifest_sha256`, `sound_count`, `updated` date.
  - Compute sha256: `shasum -a 256 openpeon.json`
  - Open PR from `fortunto2/registry` fork.

## Registry update checklist

1. Bump version in `openpeon.json`
2. Commit & push to `main`
3. Create/update git tag: `git tag -f vX.Y.Z && git push origin vX.Y.Z --force`
4. Compute: `shasum -a 256 openpeon.json`
5. Fork sync: `cd registry-fork && git fetch upstream && git reset --hard upstream/main`
6. Update silicon_valley entry in `index.json` (version, source_ref, manifest_sha256, sound_count, updated)
7. Push branch, open PR to `PeonPing/registry`
