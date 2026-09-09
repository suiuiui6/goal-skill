# Contributing

1. Create an issue describing the user-visible problem or proposal.
2. Keep changes scoped and preserve legacy compatibility.
3. Add a failing test before behavior changes.
4. Run `python -B -m pytest --rootdir . -p no:cacheprovider goal/scripts -q`.
5. Run `python -B goal/scripts/validate_goal_skill.py goal --global-agents deployment/AGENTS.md`.
6. Run `python -B tools/check_integrations.py` when linkage metadata changes.
7. Explain evidence level, limitations, and Windows enforcement wording in the PR.

Do not include `.codex` state, credentials, generated caches, production data,
or claims of observed behavior without an actual trace.
