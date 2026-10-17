# Tuning Claude

Rules that make Claude's answers shorter and easier to read.

## The problems

1. **Too much detail.** Claude answers, then adds three side points that are nice to have but don't matter.
2. **Big words.** Claude says "leverage", "robust", "delve into". People don't talk like that.

## Use it

Copy [rules/short-and-plain.md](rules/short-and-plain.md) into one of these:

- `~/.claude/CLAUDE.md` for all projects
- `CLAUDE.md` in a project for that project only

Or import it from your `CLAUDE.md`:

```
@path/to/rules/short-and-plain.md
```

## Examples

- [Too much detail](examples/too-much-detail.md)
- [Big words](examples/big-words.md)
