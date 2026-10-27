# AGENTS.md

Guidelines for AI agents working in this repository.

## What this is

**Product Ops Skills** — Agent Skills for product operations, following the [Agent Skills spec](https://agentskills.io). The repo is also a Claude Code plugin marketplace through `.claude-plugin/marketplace.json`.

- **Creator:** Charlene Strain
- **Repo:** [CharleneTStrain/product-ops-skills](https://github.com/CharleneTStrain/product-ops-skills)
- **License:** MIT

## Layout

```
product-ops-skills/
├── .claude-plugin/
│   ├── marketplace.json     # plugin marketplace manifest
│   └── plugin.json          # plugin manifest, points at ./skills
├── skills/
│   ├── product-ops-context/ # foundation skill, read by all others
│   └── skill-name/
│       ├── SKILL.md         # instructions the agent follows
│       └── README.md        # what it solves, for people
├── site/                  # the library website (index.html), published to GitHub Pages
├── validate-skills.sh
├── VERSIONS.md
├── CONTRIBUTING.md
└── README.md
```

## Checks

Skills are content only; there's no build. Run `./validate-skills.sh` after any change. It checks that:

- front matter starts the file and has `name` and `description`
- `name` matches the folder and is lowercase with hyphens, 64 characters max
- `description` is 1–1024 characters and says when to use the skill
- `SKILL.md` is under 500 lines
- every skill except `product-ops-context` has the context check
- every skill has a `## Related skills` section, and every skill it names exists

## When you change something

- Bump the skill's `metadata.version`.
- If you add, remove, or rename a skill, update the README tables, the "how skills work together" diagram, and `VERSIONS.md`, and bump the version in both files under `.claude-plugin/`.
- If you add, remove, or rename a skill, also update the skill data inside `site/index.html`.
- Keep the library's rules (see CONTRIBUTING.md): one named owner per open item, decided vs. discussed kept separate, nothing invented, plain words.
