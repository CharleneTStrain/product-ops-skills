---
name: release-notes-drafting
description: Turn engineering tickets, changelogs, PR titles or sprint summaries into customer-facing release notes. Use whenever someone asks for release notes, a changelog entry, a "what's new" post, a product update email, or a monthly product drop summary, even if they only paste raw ticket titles.
---

# Release notes drafting

Release notes exist so a customer can answer one question in under ten seconds: "Does this change anything for me?" Everything below serves that.

## Inputs to gather

Work from whatever the person provides: ticket titles, PR descriptions, a changelog, a sprint review, or notes from a product manager. Before drafting, sort every item into one of these buckets:

| Bucket | Goes in the notes? |
|---|---|
| New feature or capability | Yes, lead with these |
| Improvement to something that already exists | Yes |
| Bug fix a customer could have noticed | Yes, briefly |
| Internal refactor, tests, tooling, dependency bumps | No |
| Behind a flag or limited beta | Only if the person says so, and label it |
| Unclear | Ask, or list under "Needs confirmation" at the end |

Never invent a benefit, a metric, or a date that isn't in the source. If an item's customer impact is unclear, say so rather than guessing.

## Writing each item

For every item that goes in:

1. **Name what changed in plain words.** "You can now export reports as CSV," not "CSV export functionality."
2. **Say who it's for or where to find it**, if the source says.
3. **Say why it matters** in one sentence, only if the source supports it.

Rules:
- Lead with the verb or the outcome, not the feature name.
- One to two sentences per item. No item longer than three.
- No internal jargon, ticket IDs, team names, or codenames.
- Write "you," not "users."
- Avoid "we're excited to announce," "seamless," "powerful," "robust," "leverage."

## Output format

```
## [Product name] updates — [Month Year or version]

### New
- **[Short outcome headline].** [One or two sentences.]

### Improved
- **[Short outcome headline].** [One sentence.]

### Fixed
- [One line per fix, written as what now works.]

### Needs confirmation (internal only — remove before publishing)
- [Item] — [what's unclear]
```

Drop any section that has no items. If the person asks for a different channel (email, in-app banner, social post), keep the same sorting but shorten to the top one to three items.

## Final check

Before handing it over:
- Every item traces back to something in the source.
- Nothing internal-only slipped in.
- A customer who reads only the bold headlines still gets the gist.
