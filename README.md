> Read in: 🇺🇸 [English](README.md) | 🇧🇷 [Português (Brasil)](README.pt-BR.md)

# maxvision-skills

Curated catalog of community-contributed synthesized skills from the
[maxvision orchestrator](https://github.com/produtoramaxvision/maxvision).

This repository hosts skills that emerge from real-world combinations of
upstream agents and skills, synthesized via `synthesize-skill` and
contributed by maxvision plugin users.

## Status

**v0.0.1 — initial scaffold.** No skills landed yet. The repo exists so that
maxvision plugin users can install and reference the catalog from day one. As
synthesized skills are reviewed and merged, the `skills/` directory grows.

## Install

```text
/plugin marketplace add produtoramaxvision/maxvision-skills
/plugin install maxvision-skills@maxvision-skills
```

After install, skills appear at `~/.claude/plugins/cache/maxvision-skills/.../skills/`
and are discoverable by the maxvision orchestrator via FTS5 catalog indexing.

## Contribute

The contribution pipeline (auto-PR from synthesize-skill output) is planned for
the maxvision plugin v0.1.1 release. Manual contributions are accepted now via
direct PR following [`CONTRIBUTING.md`](CONTRIBUTING.md).

## Discoverability via maxvision plugin

The maxvision plugin catalog (`skills/discover-skill/references/skill-sources.json`)
registers this repository as a Tier 2 curated source. The orchestrator queries
it alongside other catalog sources during the route-task phase.

## License

MIT — see [`LICENSE`](LICENSE).
