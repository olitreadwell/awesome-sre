# What this revival changed

`upgundecha/awesome-sre` had not taken a pull request since 2021. This fork
carries the maintenance and runs the gate from
<https://github.com/olitreadwell/awesome-list-template>.

## The readme

- The Contents block was stale. `make toc` rebuilt it.
- 471 bullets used `*` where `-` is expected.
- The awesome badge pointed at `cdn.rawgit.com`, a dead CDN. It points at
  awesome.re.
- 45 entry links moved from http to https, each one only after https answered.
  Six were left alone: three are dead, one has no working https, and one is a
  GitHub guide rather than a repository.

## Entries

- Three books all pointed at the same landing page. The SRE book and the
  workbook point at their own tables of contents now.
- The two Hangops Slack entries linked one workspace, so they are one entry.
- Five dead entries are removed: the Azure Podcast episode, the adnanmasood
  post, the Medallia post, the Wired piece, and the SREcon17 Network World
  article.

Left alone:

- 408 entries came from upstream with a title and nothing else. The gate warns
  about them and `tests/test_readme.py` holds the count still. Adding words is
  not a revival.

## Tooling

The fork runs the same gate the engine ships. `make check` covers the list
rules, the Contents block, the GitHub stars and activity snapshot, the exports,
and the tests in `tests/test_readme.py`.
