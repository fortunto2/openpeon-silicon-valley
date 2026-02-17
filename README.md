# Silicon Valley Sound Pack

[CESP 1.0](https://openpeon.com/create) sound pack for [peon-ping](https://github.com/PeonPing/peon-ping) with quotes from **Silicon Valley**.

Russian dub by «Кубик в кубике».

## Category philosophy

- **`session.start`** — the biggest category. Energetic, expressive, memorable lines that set the mood when you open a session. Swearing welcome — this is the "hello" moment.
- **`task.complete`** — celebratory, satisfying lines. "That's what the fuck I do", "Заебись".
- **`task.acknowledge`** — calm confirmations. "I like it", "Вот именно".
- **`task.error`** — kept minimal (5 sounds). Only genuine "something broke" reactions. No expressive swearing here — those go to `session.start`.
- **`input.required`** — attention-grabbers. "Eric Bachman is a dead", "В душе не ебу".
- **`resource.limit`** — despair and limits. "Not the doors of a billionaire", "Положение хреновое".
- **`user.spam`** — kept minimal (3-4 sounds). Reserved for actual annoyance: "Говнюк", "Ты чё творишь". Expressive swearing moved to `session.start`.

## Categories breakdown

| Category | Sounds | Design intent |
|---|---|---|
| `session.start` | 22 | Loud, expressive, sets the mood |
| `task.acknowledge` | 8 | Calm confirmations |
| `task.complete` | 14 | Celebration |
| `task.error` | 5 | Minimal — genuine error reactions only |
| `input.required` | 5 | Attention-grabbers |
| `resource.limit` | 7 | Despair |
| `user.spam` | 4 | Minimal — only actual annoyance |
| **Total** | **65** | |

## Characters

**English:** Erlich Bachman, Bertram Gilfoyle, Russ Hanneman, Jian Yang

**Russian (dubbed by «Кубик в кубике»):** Richard Hendricks, Erlich Bachman, Gilfoyle, Dinesh, Russ Hanneman

## Install

```bash
git clone https://github.com/fortunto2/openpeon-silicon-valley.git \
  ~/.claude/hooks/peon-ping/packs/silicon_valley
peon packs use silicon_valley
```

If peon-ping is not installed yet:

```bash
curl -fsSL https://raw.githubusercontent.com/PeonPing/peon-ping/main/install.sh | bash
```

For Homebrew installs (packs live in `~/.openpeon/packs/`):

```bash
git clone https://github.com/fortunto2/openpeon-silicon-valley.git \
  ~/.openpeon/packs/silicon_valley
peon packs use silicon_valley
```

## Verify

```bash
peon packs list              # should show silicon_valley
peon preview --list          # list all sounds in active pack
peon preview session.start   # play a session.start sound
```

## Update

```bash
cd ~/.claude/hooks/peon-ping/packs/silicon_valley && git pull
```

## License

CC-BY-NC-4.0 — audio clips from Silicon Valley, used for personal/non-commercial purposes.
