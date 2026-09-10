---
name: sweden-accessibility-review
description: Review frontend code changes for accessibility under Swedish public-sector and consumer e-commerce rules. Use for Swedish websites, apps, public digital services, online shops, checkout, payments, identification, or accessibility statements. This is a change review, not legal advice or a full conformance audit.
---

# Swedish accessibility review

Treat `https://github.com/eli-ennab/swedish-a11y-review.git` as the
authoritative source for this review workflow and its Swedish legal baseline.
Consult it through a gitignored local mirror at `tools/swedish-a11y-review/`.

## Mandatory workflow

1. Locate the target repository root and use
   `tools/swedish-a11y-review/` beneath it as the mirror.
2. Sync the mirror before making the first accessibility judgment:
   - If `tools/swedish-a11y-review/.git` exists, run
     `git -C tools/swedish-a11y-review pull --ff-only --quiet`.
   - If the mirror does not exist, run
     `git clone --quiet --depth 1 https://github.com/eli-ennab/swedish-a11y-review.git tools/swedish-a11y-review`.
   - If the path exists but is not that Git repository, stop and explain the
     conflict instead of overwriting it.
3. If an update fails but the existing mirror contains both required documents,
   disclose that cached documents are being used. If no usable mirror exists,
   stop before making Swedish legal claims.
4. Read both of these files before reviewing:
   - `tools/swedish-a11y-review/references/review-method.md`
   - `tools/swedish-a11y-review/references/swedish-law.md`
5. Review the requested code changes according to those documents and use the
   compact report format defined in `review-method.md`. Treat the mirror as
   read-only and do not edit files inside it.
6. Record the source revision with
   `git -C tools/swedish-a11y-review rev-parse HEAD`.

## Required handoff

At the end of every review, include this line in **Review notes**:

- `Sources: [files] @ [commit SHA]`

Do not claim statutory compliance, WCAG conformance, or absence of legal risk
from a change-level or automated review.
