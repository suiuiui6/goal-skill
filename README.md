# Goal Skill (moved)

This skill now ships inside the flagship repository:

**https://github.com/suiuiui6/harness-engineering-skill/tree/main/goal**

The canonical source is `goal/` there. This repository is kept read-only so existing pins and integrations keep resolving, and it is no longer developed independently.

## Why

Three repositories competed for the same reader. The methodology, the intake skill and the enforcement CLI are one product, and the intake skill had no meaning on its own: installing it without the Harness layer gives you a router with nothing to route to.

## If you depend on this repository

- For the current skill, install `harness-engineering-skill` and use the `goal/` directory.
- Existing commit pins continue to resolve from this repository's history.
- Issue reports and pull requests should go to the flagship repository.

## License

MIT.
