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

Copy them into one of these:

- `~/.claude/CLAUDE.md` for all projects
- `CLAUDE.md` in a project for that project only

Or import them from your `CLAUDE.md`:

```
@path/to/rules/short-and-plain.md
@path/to/rules/explain.md
```

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

## Examples

- [Too much detail](examples/too-much-detail.md)
- [Big words](examples/big-words.md)
