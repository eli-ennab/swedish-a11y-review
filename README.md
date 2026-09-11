# Swedish A11y Review

Review frontend changes against WCAG and Swedish accessibility requirements for
public-sector services and consumer e-commerce.

The review covers:

- **DOS-lagen:** _DOS-lagen, eller lagen 2018:1937 om tillgänglighet till digital offentlig service_
- **LPTT/EU:s tillgänglighetsdirektiv:** _LPTT, eller lagen (2023:254) om vissa produkters och tjänsters tillgänglighet_

Depending on the project, the skill reviews against DOS-lagen, LPTT, or both.
If neither law is shown to apply, it can still perform a best-practice review
against WCAG without describing findings as legal violations.

## Install in a project

1. Copy the folder `agent-skill/swedish-a11y-review/` into your project as
   `.agents/skills/swedish-a11y-review/`.
2. Add this to the project's `.gitignore`, unless the entire `tools/` directory
   is already ignored:

```gitignore
/tools/swedish-a11y-review/
```

That is all the setup required. On first use, the skill clones this repository
into the ignored directory. The project does not need to already have a
`tools/` directory; the directory is created when needed and is only used here
as a conventional location for the local mirror. Later reviews update that copy
automatically, so they use the latest source documents. Git and network access
are required.

## Use the skill

Ask your agent to use `swedish-a11y-review`. For example, in Codex:

```text
$swedish-a11y-review Review my current frontend changes.
```

The review starts with the relevant Git changes and inspects related code and
rendered behavior when needed. It is a focused review, not a complete legal or
WCAG conformance audit.

## Source documents

- [Review method](references/review-method.md)
- [Swedish laws and legal baseline](references/swedish-law.md)
