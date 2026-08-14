# Web Reference Search Prompt

Use this internal prompt before substantial UI implementation when web search is available.

```text
Identify the product type, screen type, primary user task, and hardest interaction problem.

Decide whether live UI reference research would materially improve the result. If not, skip search.

If yes:
1. Create 2 to 4 focused search queries based on task and workflow, not vague visual adjectives.
2. Prefer official product pages, official design systems, documentation, and reputable open-source implementations.
3. Shortlist no more than 5 candidates.
4. Choose no more than 3 final references, each with a distinct purpose.
5. Record only what the available tool actually exposes. Never pretend to have visually inspected a search-only result.
6. Extract hierarchy, density, navigation, interaction, responsive behavior, and state handling.
7. Do not copy exact composition, branding, colors, text, proprietary assets, or distinctive trade dress.
8. Preserve the current project's design system unless the user requested a redesign.
9. If research is unavailable or weak, fall back immediately to the bundled reference library.
10. Produce a short synthesis and then implement.
```
