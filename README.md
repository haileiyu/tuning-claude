# Tuning Claude

Rules and settings that make Claude's answers shorter and easier to read.

## The problems

1. **Too much detail.** Claude answers, then adds three side points that are nice to have but don't matter.
2. **Big words.** Claude says "leverage", "robust", "delve into". People don't talk like that.
3. **Hard-to-read explanations.** Long walls of text where a diagram would do.

## Rules

| File | Fixes |
|------|-------|
| [rules/short-and-plain.md](rules/short-and-plain.md) | Too much detail, big words |
| [rules/explain.md](rules/explain.md) | Explanations, based on Andrej Karpathy's post (Oct 2026) |

Each file works on its own. Take one or both.

### Install for all projects

Claude Code loads every `.md` file in `~/.claude/rules/`.

```sh
mkdir -p ~/.claude/rules
cd ~/.claude/rules
curl -fsSLO https://raw.githubusercontent.com/haileiyu/tuning-claude/main/rules/short-and-plain.md
curl -fsSLO https://raw.githubusercontent.com/haileiyu/tuning-claude/main/rules/explain.md
```

Start a new session. To check, ask Claude which rules it has loaded.

### Install for one project

Do the same in `.claude/rules/` inside the project.

### Notes

- Copy the files. Do not symlink them. A symlink to a file outside the project did not load in our test.
- Rerun the `curl` lines to update.

## Settings

### Spinner says "Working"

By default the spinner shows random words like "Pondering" or "Clauding". To show only "Working", add this to `~/.claude/settings.json`:

```json
{
  "spinnerVerbs": {
    "mode": "replace",
    "verbs": ["Working"]
  }
}
```

The VS Code extension has its own setting. Add this to VS Code's user `settings.json`:

```json
{
  "claudeCode.spinnerVerbs": {
    "mode": "replace",
    "verbs": ["Working"]
  }
}
```

## Examples

- [Too much detail](examples/too-much-detail.md)
- [Big words](examples/big-words.md)
