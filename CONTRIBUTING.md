# Contributing

Thanks for helping make these skills better. Improvements to existing skills and new skills are both welcome.

## Suggest a skill

[Open a skill request](https://github.com/CharleneTStrain/product-ops-skills/issues/new?template=skill-request.yml) with the job, what you'd hand the agent, and what you'd want back.

## Add a skill

1. **Make the folder:** `skills/your-skill-name/` — lowercase, hyphens only.
2. **Write `SKILL.md`** with front matter:

   ```yaml
   ---
   name: your-skill-name
   description: What it does in one sentence. Use when [the phrases and situations that should trigger it].
   metadata:
     version: 1.0.0
   ---
   ```

   The `name` must match the folder. The description is how agents decide when to use the skill, so name the real words people say ("are we ready to launch," "log this decision").

3. **Add the context check** right after the opening paragraph — copy the `## Before you start` section from any existing skill.
4. **Write the steps.** Numbered steps, a template for the output, and the rules the output must follow.
5. **End with `## Related skills`** — two to four skills it hands off to, each with a few words on why.
6. **Write `README.md`** in the same folder: the problem, what it does, what you use it with, what you get.
7. **Add it to the README table** in the right category.
8. **Run `./validate-skills.sh`** and fix anything it flags.

## The rules every skill follows

These run through the whole library. A skill that breaks one won't be merged.

- **One named owner on every open item.** "Marketing" or "the team" is not an owner.
- **Decided and discussed stay separate.** Never present a suggestion or a lean as a decision.
- **Nothing gets invented.** If the source doesn't say why, who, or when, the output says "Not recorded."
- **Skills recommend. People decide.**
- **Plain words.** Write for someone outside the team.
- **Under 500 lines.** Move long reference material into a `references/` folder inside the skill.

## Improve a skill

Edit the `SKILL.md`, bump the patch version in its front matter (1.0.0 → 1.0.1, or 1.1.0 for a new step or output), and say in the PR what was going wrong and how the change fixes it. A before-and-after example helps a lot.

## Commit messages

Describe what the skill does or what changed for the person using it, not just the file name. "Release notes now group fixes under the product area customers see" beats "update release-notes-drafting."
