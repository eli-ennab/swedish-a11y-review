# Swedish accessibility review method

Review the relevant Git diff and rendered behavior for accessibility
regressions. Apply the correct Swedish regime before attaching legal
significance to a finding.

## Establish scope

Classify the project as one or more of:

- **Public digital service:** potentially subject to lag (2018:1937) om
  tillganglighet till digital offentlig service (DOS-lagen).
- **Consumer e-commerce:** potentially subject to lag (2023:254) om vissa
  produkters och tjansters tillganglighet (LPTT) and PTSFS 2024:6.
- **Both:** for example, a public actor offering an in-scope consumer service.
- **Voluntary review:** no legal regime is established, but Swedish
  accessibility best practice is requested.

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

Lead with findings, ordered by severity. For each finding include:

- classification and severity
- file and line, route, component, or journey
- observed evidence and affected users
- applicable Swedish regime and exact provision or technical standard clause
  when established
- related WCAG success criterion and level when useful
- a minimal remediation and a concrete verification method

Then include:

- **Scope used:** public sector, consumer e-commerce, both, or voluntary; list
  assumptions.
- **Checks performed:** code inspection, commands, rendered tests, and assistive
  technology used.
- **Manual checks remaining:** especially keyboard flow, screen-reader
  announcements, content alternatives, contrast, zoom/reflow, cognitive
  clarity, and third-party checkout or identity flows.
- **No findings:** if applicable, state only that no issues were identified in
  the reviewed scope. Never call that conformance.

Report in the user's language while retaining the official Swedish names of
laws and authorities. Cite current official sources when making legal claims in
a user-facing report.
