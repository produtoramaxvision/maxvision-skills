# Contributing to maxvision-skills

This repository accepts curated, MIT-compatible synthesized skills from the
maxvision orchestrator.

## Scope

Skills here are derivative works that combine two or more upstream skills or
agents into a single new skill that generalizes beyond a single use case.

## Quality gate

PRs must include:

- A `skills/<skill-name>/SKILL.md` file with valid Anthropic Agent Skills 2.0
  frontmatter (`name`, `description`, `when_to_use`).
- A clear explanation (≥80 chars) of the gap this skill fills and why a
  combination is more valuable than individual upstream skills.
- MIT-compatible license attribution for every upstream source the skill
  derives from.
- No proprietary code, internal hostnames, environment variables containing
  credentials, or other private data.

CI validates JSON syntax, markdown lint, and SKILL.md presence. PRs that fail
CI are auto-closed after 30 days of inactivity.

## Manual contribution (for now)

Until the maxvision plugin v0.1.1 ships the auto-PR pipeline, contributions go
through the standard GitHub fork → branch → PR flow:

```bash
gh repo fork produtoramaxvision/maxvision-skills --clone=true
cd maxvision-skills
git checkout -b synth/<skill-name>
mkdir -p skills/<skill-name>
cp ~/.claude/skills/<skill-name>/SKILL.md skills/<skill-name>/
git add skills/<skill-name>
git commit -m "feat(skill): add <skill-name>"
git push -u origin synth/<skill-name>
gh pr create --base main
```

## License

By submitting a PR you confirm the skill is your work or derived from
MIT-compatible upstreams, and you license your submission under the MIT
license. See [`LICENSE`](LICENSE).
