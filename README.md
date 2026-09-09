# Goal Skill

[![CI](https://github.com/suiuiui6/goal-skill/actions/workflows/ci.yml/badge.svg)](https://github.com/suiuiui6/goal-skill/actions/workflows/ci.yml)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

Project intake and governance routing for evidence-first AI coding delivery.

> 中文：Goal Skill 负责项目目标接收、bootstrap/maintenance 分类、起始层选择、
> 用户确认门禁和结构化关闭。它不会取代 Harness 的分层执行，也不会把静态检查、
> synthetic 记录或退出码 0 冒充真实交付证据。

## Repository role

This repository is the canonical public source for the `goal` Codex Skill.
The installable package lives in [`goal/`](goal/).

- [goal-skill](https://github.com/suiuiui6/goal-skill) owns Goal intake, protocol, capability discovery, and handoff.
- [harness-engineering-skill](https://github.com/suiuiui6/harness-engineering-skill) owns layer execution, gates, rollback, and closure.
- [goal-harness-web-fullstack](https://github.com/suiuiui6/goal-harness-web-fullstack) owns version-pinned integration, Guard/Delivery contracts, full-stack fixtures, and release evidence.

These repositories complement each other and do not conflict. Goal hands approved
project work to Harness; the Fullstack repository verifies the compatible combination.

## Validate

Clone the repository and validate the package before installing only `goal/` as the
Codex Skill directory:

```powershell
python -B goal/scripts/validate_goal_skill.py goal
python -B -m pytest --rootdir . -p no:cacheprovider goal/scripts -q
```

Governed mutation and delivery modes additionally require a compatible Harness Skill
and Goal Guard. Windows enforcement is `audit-only-windows`; unavailable hooks are
never claimed as mechanical blocking.

## Integration contract

Machine-readable relationships are recorded in [`integrations.json`](integrations.json).
The Fullstack repository pins an exact Goal commit before integration testing,
preventing silent source drift. Companion `tested_commit` values record known
compatibility evidence; only the Fullstack integration manifest owns current-HEAD pins.

## Evidence boundaries

- Contract checks prove package structure and rule invariants.
- Recorded event replay proves only the events actually observed.
- Full-stack fixtures prove only the isolated combinations they execute.
- Missing live Agent+Skill observation remains `not-run`.

See [CONTRIBUTING.md](CONTRIBUTING.md), [SECURITY.md](SECURITY.md), and
[CHANGELOG.md](CHANGELOG.md).
