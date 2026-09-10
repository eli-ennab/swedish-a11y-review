# swedish-a11y-review

Review the relevant Git diff and rendered behavior for accessibility
regressions. Apply the correct Swedish regime before attaching legal
significance to a finding.

## Establish scope

Classify the project as one or more of:

- **Public digital service:** potentially subject to the law (2018:1937) about
  "Tillgänglighet till digital offentlig service" (DOS-lagen).
- **Consumer e-commerce:** potentially subject to the law (2023:254) about "Vissa
  produkters och tjänsters tillgänglighet" (LPTT) and PTSFS 2024:6.
- **Both laws may apply:** assess DOS-lagen and LPTT independently.
- **Best-practice only:** neither law has been shown to apply; review against
  accessibility and WCAG guidance without describing findings as legal violations.

Infer scope from repository evidence when possible. Consider the actor,
intended users, B2C versus B2B purpose, service type, release date, third-party
control, and documented exemptions. If a fact would materially change the
legal classification and cannot be inferred, state the alternative conclusions
or ask one narrow question. Never assume that a small business, third-party
component, legacy page, or disproportionate burden is exempt.

Use [swedish-law.md](swedish-law.md) when determining legal scope or describing
a finding as legally required. Verify current official sources when internet
access is available because legislation, regulations, and referenced standards
can change.

## Evidence

Use the smallest scope that establishes the behavior:

1. Read the relevant staged, unstaged, committed, or branch diff and identify
   affected user journeys.
2. Inspect templates, components, styles, routes, state changes, shared code,
   and third-party integrations needed to understand those journeys.
3. Discover existing accessibility tooling and project test commands. Run
   relevant existing checks when safe and authorized; do not install packages
   or alter configuration merely to perform a review.
4. If the application can run, exercise the changed journey with keyboard-only
   input and inspect focus, names, roles, states, errors, status updates,
   zoom/reflow, contrast, and responsive variations as applicable.
5. Identify checks that require human judgment or assistive-technology testing.
   Automated tools cannot establish overall accessibility or legal conformity.

Consider axe, Accessibility Insights, Playwright, pa11y, Lighthouse, framework
lint rules, browser accessibility trees, screen readers, zoom or magnification,
high-contrast modes, and voice control only when relevant and available.

## Review coverage

Review applicable changes for:

- semantics, structure, names, roles, states, values, and ARIA validity
- keyboard operation, logical order, traps, shortcuts, and alternatives to
  pointer gestures
- visible focus, focus movement, focus restoration, and obscured focus
- labels, instructions, autocomplete, validation, error prevention, and status
  messages
- text alternatives, captions, audio description, animation, flashing, and
  time limits
- contrast, use of color, resizing, reflow, orientation, text spacing, and
  target size
- headings, landmarks, links, buttons, tables, lists, dialogs, and navigation
  consistency
- compatibility with browsers, screen readers, magnification, voice control,
  and other assistive technology

Prefer native semantics and behavior over custom ARIA implementations.

For consumer e-commerce, trace the complete path from product discovery through
contract completion. Review accessibility information for products and
services, identification, electronic signatures, security, and payment even
when a third party supplies a step.

For public digital service, check whether the change affects the accessibility
statement, feedback mechanism, access to excluded content, documents, or other
EN 301 549 requirements beyond WCAG.

## Legal precision

- Do not equate WCAG with Swedish law. State the applicable law, regulation, or
  standard separately from the supporting WCAG success criterion.
- For DOS-lagen, use the version of EN 301 549 incorporated by Digg's current
  rules; do not silently substitute WCAG 2.2.
- For LPTT, distinguish a direct functional or sector-specific requirement
  from standards used only as implementation guidance or a possible
  presumption of conformity.
- Describe an issue as a **confirmed legal requirement** only when scope and the
  controlling requirement are established. Otherwise use **potential legal
  issue**, **technical accessibility defect**, or **manual verification
  required**.
- Do not claim statutory compliance, WCAG conformance, or absence of legal risk
  from a change-level or automated review.
- Do not provide legal advice. Recommend qualified legal review for disputed
  scope, exemptions, enforcement exposure, or formal conformity claims.

## Finding classifications

- **Confirmed:** evidence demonstrates a defect in source or rendered behavior.
- **Potential:** likely defect, but missing runtime, content, third-party, or
  scope evidence prevents confirmation.
- **Manual check:** cannot be reliably decided from code or automation.

Use critical, high, medium, or low severity based on user impact, journey
importance, reach, and availability of a workaround. Do not base severity
solely on WCAG level.

## Output

Keep the report short and easy to scan. Do not repeat the review method, provide
a general accessibility tutorial, or summarize legislation before the
findings. Group occurrences with the same cause and remediation into one
finding. Do not omit a material finding merely to shorten the report.

Lead with findings in severity order. Use this compact format for each one:

```text
### [High] Short problem title — Confirmed
`path/to/file:line` · affected component or journey

Problem: What happens and who is affected.
Basis: DOS-lagen 10 § · EN 301 549 clause · WCAG criterion, as applicable.
Fix: The smallest practical correction.
Verify: One concrete test.
```

Use only applicable legal and technical references in `Basis`; omit labels that
are not established or useful. Keep each field to one or two sentences. Link an
official legal source once per applicable law, not repeatedly in every finding.

Finish with a compact **Review notes** section containing only:

- **Scope:** applicable regime and material assumptions
- **Checked:** code, commands, or rendered behavior actually examined
- **Still manual:** only important checks that remain unresolved
- **Sources:** documents consulted and source revision

Omit `Still manual` when nothing material remains. Do not include a long list of
checks that passed. If there are no findings, say: `No accessibility issues were
identified in the reviewed scope.` Then include the review notes and make clear
that this is not a conformance finding.

Report in the user's language while retaining the official Swedish names of
laws and authorities. Cite current official sources when making legal claims in
a user-facing report.
