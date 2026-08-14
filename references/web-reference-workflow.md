# Web Reference Workflow

Use this workflow only when web search is available and useful. The goal is to discover current, task-relevant UI/UX patterns without creating a paid dependency.

## 1. Decide Whether Search Is Worth It

Search for substantial or unfamiliar interface work such as:

- complex dashboards
- developer consoles
- AI workspaces
- commerce flows
- billing and subscription management
- onboarding
- advanced search and filtering
- dense tables
- permission systems
- mobile navigation
- unfamiliar domain-specific workflows

Usually skip search for ordinary buttons, simple forms, basic dialogs, and minor style fixes when the existing product already establishes the pattern.

## 2. Build Search Intents

Search by task and interaction, not by visual adjective.

Good intents:

- developer platform project settings permissions UI
- SaaS audit log filter table UX
- AI chat workspace source citations interface
- subscription billing usage limits settings UI
- mobile inventory scanner workflow UI

Weak intents:

- beautiful dashboard
- cool modern UI
- best glassmorphism design
- trendy website

## 3. Prefer Strong Sources

Use this order when possible:

1. official product pages and documentation
2. official design systems and component documentation
3. public product help centers containing screenshots
4. reputable open-source applications and repositories
5. high-quality public case studies
6. broad inspiration galleries only as a last resort

## 4. Select at Most Three References

Each reference must have a job. For example:

- Reference A: information hierarchy and density
- Reference B: interaction model and edge states
- Reference C: responsive behavior or complex component pattern

The current project remains the source of truth for brand, typography, color, spacing, radius, iconography, and voice unless the user asks for a redesign.

## 5. Extract Patterns, Not Pixels

For each accessible reference record:

- source/product
- why it is relevant
- pattern being borrowed
- what should not be copied
- adaptation required for this product
- confidence level based on what was actually accessible

Examples of useful extraction:

- persistent filters for a high-frequency table
- summary row above detailed data
- progressive disclosure for advanced settings
- inline validation near the affected field
- command palette for high-frequency navigation
- mobile bottom sheet replacing a wide desktop popover

Do not extract exact colors, spacing values, text, icons, illustrations, or distinctive branded composition unless they belong to the current project.

## 6. Handle Search-Only Results Correctly

Some search providers expose titles, URLs, and snippets but cannot read page content. In this mode:

- never claim to have inspected the visual layout
- do not infer exact component placement from a title or snippet
- use the result only to identify candidate products or documentation
- rely on local library guidance for implementation if the page cannot be inspected
- use user-provided screenshots or accessible documentation when available

## 7. Freshness

For products that change frequently, prefer recent public material. Do not assume an old screenshot still represents the current interface.

Freshness matters most for:

- AI products
- developer platforms
- dashboards and admin products
- rapidly changing SaaS tools

For stable platform guidance such as accessibility concepts and native interaction conventions, official documentation can remain useful even when not newly published.

## 8. Synthesize

Before coding, reduce research to a short internal reference brief:

```text
Screen job: ...
Reference A: ... -> learn ...
Reference B: ... -> learn ...
Reference C: ... -> learn ...
Keep from current product: ...
Avoid: ...
Final synthesis: ...
```

Then implement the product-specific solution.
