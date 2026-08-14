# Web Research Rules

## Free-First Policy

Live research is optional. Never require a paid UI reference API or paid design database. If available web search would cost the user money and they have not requested that capability, use the bundled reference library instead.

If a free or already-enabled search capability exists, it may be used for substantial UI work.

## Evidence Discipline

Only claim to have analyzed what the available tool actually exposed.

- Search result only: title, URL, snippet, and displayed metadata only.
- Parsed page: textual page structure and content may be analyzed.
- Screenshot/image: visible layout and visual hierarchy may be analyzed.
- Repository/source code: implementation patterns may be analyzed when accessible.

Never describe an inaccessible page's exact layout as if it was seen.

## Search Budget

Keep research lightweight:

- start with 2 to 4 focused queries
- shortlist 2 to 5 candidates
- use no more than 3 final references
- stop searching once the important design decisions have enough evidence

Do not turn routine UI implementation into open-ended browsing.

## Query Quality

Search for product type + user task + component or workflow.

Prefer:

`B2B permissions role editor UI`

Over:

`beautiful SaaS UI inspiration`

## Source Quality

Prefer official and primary sources. Open-source implementations are preferred when implementation details matter. Use galleries only for broad visual exploration and never as the sole basis for usability claims.

## Anti-Cloning

References are evidence for patterns, not permission to reproduce another product. Do not copy:

- logos or brand marks
- proprietary illustrations
- exact marketing copy
- exact page composition
- distinctive branded graphics
- trademarked visual identity
- proprietary assets

Do not intentionally make a confusingly similar clone.

## Attribution in Work Notes

When the agent reports reference research to the user, name the reference products or source types used and describe the borrowed concepts at a high level. Do not overwhelm normal implementation responses with a bibliography unless requested.

## No Search Failure Mode

If search is unavailable, disabled, rate-limited, blocked, or too weak to inspect candidates:

1. continue without blocking
2. use the current product first
3. use `references/library.md` and `references/component-patterns.md`
4. state the limitation only when it materially affects confidence

## Persian and RTL

If reference research includes Persian or RTL products, do not blindly copy their typography or spacing. Apply `rules/rtl.md` and `rules/persian-text.md`. Persian output must not contain U+200C. Use normal spaces instead.
