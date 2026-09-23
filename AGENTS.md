# Agent instructions

This repository is one person's curated list. The rules it follows live in the
engine at <https://github.com/olitreadwell/awesome-list-template>, and
`README.md` is the only source of truth for entries.

## Before you change anything

```bash
uv sync --group dev
make hooks-install
make check
```

## Rules

- Every entry is `- [Name](https://example.com/) - What it is.` with a capital
  and a closing period. This list does not use tags.
- Do not write entry text with a model. 408 entries came from upstream with a
  title and nothing else, and those words are a person's to write.
- Check a link by hand before you touch it. Entries that were already dead when
  the fork was made are recorded in docs/revival.md rather than guessed at.
- Run `make toc` after moving a heading, and never hand-edit Contents lines.
- Give every GitHub link its stars and last-push date with `make stats`. Never
  hand-write a stars number. `make stats-check` verifies the snapshot offline.

## Layout

- `README.md` holds the list, the Contents section, and the prose.
- `civic-tech.md` is a raw link list kept from upstream for reference. It is not
  checked and it is not part of the list contract.
- `tests/test_readme.py` holds the invariants for this particular list.
- `docs/revival.md` records what the engine changed and what it left alone.
