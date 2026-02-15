# Silicon Valley Sound Pack

[CESP 1.0](https://openpeon.com/create) sound pack for [peon-ping](https://github.com/PeonPing/peon-ping) with quotes from HBO's **Silicon Valley** (Кремниевая долина).

## 58 sounds

- **18 English** — Erlich Bachman, Gilfoyle, Russ Hanneman, Jian Yang
- **40 Russian** (dubbed) — best moments, coding-themed phrases

### Sample quotes

| Category | Examples |
|---|---|
| `session.start` | "This guy fucks!", "Добро пожаловать в долину", "Новый интернет" |
| `task.acknowledge` | "Three commas.", "Вот именно", "Я решил, слышишь", "Не усну пока не закончу" |
| `task.complete` | "That's what the fuck I do.", "Заебись", "Победитель с большим отрывом" |
| `task.error` | "Holy shit.", "Ёбушки-воробушки", "Проекту конец", "Хреновая идея" |
| `input.required` | "Eric Bachman is a dead.", "В душе не ебу", "Что происходит" |
| `resource.limit` | "These are not the doors of a billionaire.", "Положение хреновое" |
| `user.spam` | "You just brought piss to a shit fight.", "Нахуй пошёл", "Бедное мудачьё" |

## Install

### Option 1: One-liner (recommended)

```bash
git clone https://github.com/fortunto2/openpeon-silicon-valley.git \
  ~/.claude/hooks/peon-ping/packs/silicon_valley
```

Then activate:

```bash
peon packs use silicon_valley
```

### Option 2: If peon-ping not installed yet

Install [peon-ping](https://github.com/PeonPing/peon-ping) first:

```bash
curl -fsSL https://raw.githubusercontent.com/PeonPing/peon-ping/main/install.sh | bash
```

Then clone this pack:

```bash
git clone https://github.com/fortunto2/openpeon-silicon-valley.git \
  ~/.claude/hooks/peon-ping/packs/silicon_valley
peon packs use silicon_valley
```

### Option 3: Manual copy

```bash
git clone https://github.com/fortunto2/openpeon-silicon-valley.git /tmp/sv-pack
cp -r /tmp/sv-pack/sounds /tmp/sv-pack/openpeon.json \
  ~/.claude/hooks/peon-ping/packs/silicon_valley/
rm -rf /tmp/sv-pack
peon packs use silicon_valley
```

### Homebrew / ~/.openpeon installs

If peon-ping was installed via Homebrew, packs live in `~/.openpeon/packs/`:

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

## Categories breakdown

| Category | EN | RU | Total |
|---|---|---|---|
| `session.start` | 3 | 4 | 7 |
| `task.acknowledge` | 2 | 7 | 9 |
| `task.complete` | 3 | 6 | 9 |
| `task.error` | 3 | 11 | 14 |
| `input.required` | 3 | 2 | 5 |
| `resource.limit` | 2 | 5 | 7 |
| `user.spam` | 2 | 5 | 7 |
| **Total** | **18** | **40** | **58** |

## Characters

**English:** Erlich Bachman, Bertram Gilfoyle, Russ Hanneman, Jian Yang

**Russian (dubbed):** Ричард Хендрикс, Эрлих Бахман, Гилфойл, Динеш, Расс Ханнеман

## License

CC-BY-NC-4.0 — audio clips from HBO's Silicon Valley, used for personal/non-commercial purposes.
