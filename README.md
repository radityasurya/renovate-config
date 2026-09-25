# renovate-config

Shared Renovate presets for `radityasurya` repositories.

## Presets

- `default.json` — the base preset for every repo. Weekly schedule
  (Monday before 6 a.m., Europe/Amsterdam), 3-day minimum release age,
  grouped non-major updates, and automerge of minor and patch updates.
- `no-ci.json` — disables automerge. Extend this preset in addition to the
  base preset when a repo has no CI that runs on pull requests. Without CI,
  nothing tests an update before it merges, so a human reviews every PR.

## Usage

In a repo with pull-request CI, use:

```json
{ "extends": ["github>radityasurya/renovate-config"] }
```

In a repo without pull-request CI, use:

```json
{ "extends": ["github>radityasurya/renovate-config", "github>radityasurya/renovate-config:no-ci"] }
```
