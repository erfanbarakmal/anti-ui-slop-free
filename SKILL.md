---
name: anti-ui-slop-free
description: A free-first UI/UX reference and quality skill for coding agents. Prevents generic AI-looking interfaces, preserves existing design systems, optionally researches fresh public UI references when web search is available, falls back to a local reference library, enforces responsive/accessibility states, and performs a final visual critique without requiring any paid API.
version: 3.0.0
license: MIT
---

# Anti UI Slop Free

Build interfaces that feel specific to the product, task, platform, and existing design system instead of defaulting to generic AI-generated UI patterns.

This skill is intentionally local-first and dependency-free. It does not require UIZZE, a paid reference API, a hosted service, or a proprietary dataset.

## Core Principle

The coding agent remains responsible for design decisions.

Do not optimize for novelty. Optimize for clarity, specificity, usability, coherence, accessibility, and fit with the product.

A familiar UI pattern is acceptable when it is the clearest solution. Do not make an interface stranger, louder, more decorative, or more complex merely to prove that this skill was used.

## Non-Negotiable Rules

1. Inspect before designing.
2. Reuse the existing design system before inventing new visual language.
3. Do not add unnecessary sections, copy, labels, metrics, controls, routes, badges, cards, gradients, or decorative motifs.
4. Every visible control must have a real function or a clear implementation path.
5. Treat mobile and narrow layouts as first-class, not as a desktop shrink pass.
6. Implement relevant loading, empty, error, disabled, hover, focus, active, selected, success, and destructive states.
7. Prefer semantic HTML and accessible interaction patterns.
8. Perform a final visual critique after the first substantial implementation.
9. Fix high-impact visual and interaction problems before declaring the UI complete.
10. For Persian text, never use Unicode half-space / ZWNJ (U+200C). Use a normal space (U+0020) between words instead.
11. For substantial UI work, classify the project and screen, then choose up to three conceptual references for different purposes.
12. References may guide hierarchy, density, interaction, states, and responsive behavior, but must never be used for direct visual cloning.

## The Workflow

### Move 1 — Inspect the Product

Before writing substantial UI code, inspect the project for:

- app purpose and primary user task
- existing layout conventions
- component library
- typography
- spacing scale
- color tokens
- radius and border conventions
- icon system
- navigation model
- existing responsive behavior
- data density
- common interaction patterns
- product-specific vocabulary

If the project already has a coherent system, preserve it.

Do not replace an existing visual system with your own preferred aesthetic unless the user explicitly asks for a redesign.

### Move 2 — Define the Interface Job

Write a brief internal design intent before coding:

- What is the main task on this screen?
- What information is primary?
- What is secondary?
- What must be visible immediately?
- What can be progressive disclosure?
- What is the most important action?
- What could confuse the user?

Use this intent to determine hierarchy.

### Move 2.5 — Research and Route to Useful References

For substantial UI work, classify the project and screen using `references/project-router.md`.

If web search is available, apply `references/web-reference-workflow.md` and `rules/web-research.md` before selecting references. Search for a small set of current, task-relevant public references. If web search is unavailable, weak, search-only, blocked, or would require a paid capability the user did not request, skip it and use the local library. Never block UI implementation on web research.

Then choose up to three references from fresh research, `references/library.md`, or both. Prefer a mix such as:

- one reference for hierarchy or density
- one for interaction or state handling
- the current product for visual language

Use `rules/reference-use.md` to prevent cloning.

When the interface is Persian-first or RTL, also apply `rules/rtl.md`.

### Move 3 — Choose Patterns Deliberately

Select layout and interaction patterns because they fit the product, not because they are common in generated dashboards.

Avoid automatic use of:

- hero + three feature cards
- oversized gradient headline text
- glassmorphism panels
- floating gradient blobs
- excessive rounded cards
- every section inside a card
- stat cards without a real decision-making purpose
- giant whitespace that reduces useful information density
- decorative badges above headings
- fake charts
- fake analytics
- meaningless activity feeds
- redundant sidebars
- redundant top navigation plus sidebar navigation
- giant CTA buttons for routine actions
- emoji as interface icons
- Unicode symbols as substitute UI icons
- excessive pills for ordinary labels
- excessive shadow layers

Cards are allowed when grouping, containment, scanning, or interaction genuinely benefits from them.

### Move 4 — Implement the Real States

For each interactive or data-driven region, determine which states are relevant:

- initial
- loading
- loaded
- empty
- partial data
- error
- offline or unavailable when applicable
- disabled
- hover
- keyboard focus
- active / pressed
- selected
- success
- destructive confirmation

Never design only the ideal loaded state when the product requires more.

### Move 5 — Responsive and Accessibility Pass

Check at minimum:

- narrow mobile width
- wider mobile width
- tablet-like width when relevant
- desktop width
- long labels
- localized text expansion
- keyboard navigation
- visible focus
- form labels
- error association
- contrast
- touch target size
- reduced motion when animation exists

Navigation must adapt on narrow screens. Do not merely clip it or push actions off-screen.

### Move 6 — Final Anti-Slop Critique

After the first substantial render or implementation, review the screen as if you did not write it.

Ask:

- Does this look like a generic template?
- Is the hierarchy obvious in three seconds?
- Are there too many cards?
- Are there unnecessary containers?
- Are there decorative elements with no functional value?
- Is useful information density too low?
- Are components consistent with the rest of the project?
- Does the layout reflect the actual user task?
- Are the important actions visually prioritized?
- Are secondary actions too loud?
- Does mobile feel intentionally designed?
- Are all states covered?
- Is any copy generic or filler-like?
- Are controls real and usable?

Fix the highest-impact issues before completion.

## Visual Reference Strategy Without Paid APIs

Supporting files:
- `references/web-reference-workflow.md` — free-first live reference discovery workflow
- `rules/web-research.md` — evidence, freshness, attribution, and fallback rules
- `prompts/web-reference-search.md` — reusable reference search prompt
- `checklists/web-reference-pass.md` — live research validation
- `references/library.md` — product and pattern reference library
- `references/project-router.md` — classify project and screen before selecting references
- `references/component-patterns.md` — component-level pattern guidance
- `rules/reference-use.md` — anti-cloning constraints
- `checklists/reference-pass.md` — pre-build reference validation
- `prompts/reference-analysis.md` — reusable internal analysis prompt


When references are useful, use sources available to the project or user without requiring a paid service:

1. Existing screens in the same product.
2. Existing design files or screenshots supplied by the user.
3. Existing component stories or Storybook.
4. Public product screenshots when browsing is available and appropriate.
5. Open-source applications with a similar task model.
6. Platform-native patterns for web, iOS, Android, or desktop.

Use references to understand hierarchy, density, navigation, interaction, and state design.

Do not copy a product's brand identity, proprietary illustrations, distinctive trade dress, or exact visual composition.

## Free-First Web Reference Mode

When a web search capability exists, use it as an optional enhancement, not a dependency.

Priority order:

1. Current product and existing design system.
2. User-provided screenshots, links, mocks, and design files.
3. Fresh public references discovered through available web search.
4. Local reference library bundled with this skill.
5. Platform conventions and component-library documentation.

Do not ask the user to buy a search product, reference API, or design database in order to complete normal UI work.

Search only when it will materially improve a substantial UI decision. Do not search for every button or common component.

When search results cannot provide full page content, use only facts actually visible in search metadata/snippets. Do not pretend to have inspected layouts that were not accessible.

Prefer official product pages, official design systems, public documentation, reputable open-source projects, and user-supplied references. Avoid low-quality SEO galleries when stronger sources exist.

Never copy exact branding, proprietary assets, illustration systems, trademarked identity, or distinctive page compositions. Synthesize patterns into the current product's visual language.

## Hierarchy Rules

- The primary heading should normally be the first meaningful text in a page or section.
- Do not add decorative eyebrow labels above headings unless they convey necessary context.
- One region should have one clear primary action.
- Secondary actions should visually remain secondary.
- Use typography, spacing, alignment, and grouping before reaching for borders, shadows, and background fills.
- Do not use color as the only carrier of meaning.

## Layout Rules

- Prefer a small number of meaningful regions over many independent cards.
- Align to a consistent grid.
- Reuse spacing tokens.
- Avoid arbitrary one-off pixel values when a token exists.
- Avoid unnecessary nested containers.
- Avoid full-width content when readable measure matters.
- Avoid tiny content columns when the task is data-dense.
- Do not center everything by default.
- Match alignment to task: reading content often benefits from left alignment; dashboards often benefit from strong column alignment.

## Typography Rules

- Reuse the project's type scale and fonts.
- Keep hierarchy visible without extreme size jumps.
- Avoid oversized marketing typography inside utility/product screens.
- Do not use all-caps excessively.
- Keep labels concise and concrete.
- Avoid filler copy written only to make the composition look complete.

## Color and Effects Rules

- Reuse existing tokens before adding new colors.
- Use gradients only when justified by the product's visual language.
- Avoid glow effects unless the product already uses them meaningfully.
- Keep shadows subtle and structural.
- Prefer borders, spacing, or tonal grouping when they communicate structure more clearly.
- Do not use random accent colors to make a screen appear more designed.

## Icon Rules

- Reuse the project's icon library.
- Use icons only when they improve scanning or save space without harming clarity.
- Provide accessible names for icon-only controls.
- Do not use emoji as interface icons unless the product intentionally uses emoji as content.
- Do not use decorative Unicode glyphs as pseudo-icons.

## Data UI Rules

- Never invent metrics or charts unless the user asked for placeholders or mock data.
- Do not create a dashboard merely because the project contains data.
- Choose tables when comparison across rows and columns matters.
- Choose lists when order and scanning matter more than comparison.
- Choose charts only when visual comparison or trend recognition adds value.
- Show units, time ranges, and context when metrics could otherwise be ambiguous.
- Empty states should explain what happened and what the user can do next.

## Forms Rules

- Use visible labels when ambiguity is possible.
- Use placeholder text as an example, not as the only label.
- Place validation feedback near the relevant field.
- Keep required/optional conventions consistent.
- Preserve entered data after recoverable errors.
- Disable submit only when the reason is obvious, otherwise explain the requirement.
- Make destructive actions explicit.

## Motion Rules

- Animation must communicate change, hierarchy, causality, or spatial relationship.
- Avoid animation used only to make the interface feel premium.
- Prefer short, restrained transitions.
- Respect reduced-motion preferences.
- Never delay user input for decorative animation.

## Persian Text Rule

When generating Persian or mixed Persian UI copy:

- Never output U+200C ZERO WIDTH NON-JOINER (ZWNJ / half-space).
- Use U+0020 SPACE instead.
- Example: write `می شود`, not `می شود`.
- Example: write `آن ها`, not `آن ها`.
- Example: write `دکمه های`, not `دکمه های`.
- Before completion, scan generated text files for U+200C and replace every occurrence with a normal space unless the user explicitly overrides this project rule.

Recommended check:

```bash
# Find Persian half-space / ZWNJ occurrences
rg -n $'\u200c' .
```

Recommended automatic cleanup when appropriate:

```bash
python - <<'PY'
from pathlib import Path
for path in Path('.').rglob('*'):
    if path.is_file():
        try:
            text = path.read_text(encoding='utf-8')
        except Exception:
            continue
        if '\u200c' in text:
            path.write_text(text.replace('\u200c', ' '), encoding='utf-8')
PY
```

## Definition of Done

The UI is not done until:

- the primary task is clear
- the hierarchy is intentional
- the UI fits the existing product system
- unnecessary visual decoration is removed
- controls are functional
- relevant states exist
- responsive behavior is intentional
- keyboard and focus behavior are reasonable
- accessibility issues found during implementation are addressed
- Persian text contains no U+200C when Persian is present
- the final anti-slop critique has been performed

Read the supporting files in this skill when deeper guidance is needed:

- `rules/layout.md`
- `rules/visual-language.md`
- `rules/components.md`
- `rules/states.md`
- `rules/accessibility.md`
- `rules/persian-text.md`
- `checklists/pre-build.md`
- `checklists/final-review.md`
- `references/reference-method.md`
- `prompts/critique.md`
