# Swedish A11y Review

Review frontend changes against Swedish accessibility laws, standards, and
WCAG guidance.

## Use it in another repository

1. Copy `agent-skill/sweden-accessibility-review/` to
   `.agents/skills/sweden-accessibility-review/` in the target repository.
2. Add this to the target repository's `.gitignore`:

```gitignore
tools/swedish-a11y-review/
```

The skill clones or updates this repository in that gitignored directory, so
each review uses the latest source documents. The first run requires Git and
network access.

## Run it

Invoke `sweden-accessibility-review` using your agent's skill syntax. For
example, in Codex:

```text
$sweden-accessibility-review Review my current frontend changes.
```

## Source documents

- [Review method](references/review-method.md)
- [Swedish legal baseline](references/swedish-law.md)
