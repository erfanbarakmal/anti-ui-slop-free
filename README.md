# anti-ui-slop-free

A free, local-first UI and UX skill for coding agents that helps prevent generic AI-looking interfaces and teaches the agent to synthesize useful patterns from multiple product references without cloning them.

## Features

- No paid API required
- No UIZZE dependency
- Existing-design-system-first workflow
- Anti-template / anti-slop rules
- Responsive UI checks
- Accessibility checks
- Loading / empty / error / interaction state coverage
- Final visual critique workflow
- Built-in reference library by product type and UI job
- Component pattern guide
- Reference router for dashboards, settings, forms, chat, commerce, onboarding, and more
- Anti-cloning rules for reference use
- RTL and Persian UI guidance
- Persian rule: no U+200C half-space; normal spaces only

## Suggested Installation

Copy this directory into the skills/instructions directory supported by your coding agent, or add `SKILL.md` and the supporting files to the repository's agent instructions.

Because skill locations and discovery behavior differ between tools and versions, follow the current documentation for your specific coding agent.

## Minimal Usage Instruction

Tell your agent:

> Use the anti-ui-slop-free skill for all substantial UI work. Inspect the existing product before designing, preserve its system, implement relevant states and responsive behavior, then run the final critique. Persian output must never contain U+200C; use ordinary spaces instead.

## License

MIT. You may modify and use this skill in your own projects.


## Reference Workflow

For substantial UI work, the agent should:

1. inspect the current product
2. classify the project type and screen job
3. select up to three references for different purposes
4. extract hierarchy, density, interaction, state, and responsive principles
5. keep the current product as the visual source of truth
6. synthesize rather than clone
7. run the final anti-slop critique

Example:

- Linear for navigation density
- Stripe for data presentation
- GitHub for filters and row actions
- current product for colors, typography, spacing, radius, and icons

The final UI should not look like any single reference product.
