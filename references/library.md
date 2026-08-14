# Reference Library

Use this library to choose patterns intentionally. References are conceptual, not templates to copy.

## Product Families

### SaaS and B2B
Useful references: Linear, Vercel, Stripe Dashboard, GitHub, Notion.
Study:
- dense but readable information hierarchy
- clear primary navigation
- restrained use of cards
- strong table and list patterns
- compact command and action placement
Avoid copying:
- logos, brand colors, exact spacing, proprietary illustrations, distinctive page compositions

### Developer Tools
Useful references: GitHub, Supabase, Railway, Vercel, Cloudflare Dashboard.
Study:
- repository or project navigation
- environment and deployment status
- logs, tables, filters, command surfaces
- error and empty-state clarity
- progressive disclosure for advanced controls

### AI Products
Useful references: ChatGPT, Claude, Perplexity, Cursor.
Study:
- conversation hierarchy
- prompt and composer ergonomics
- source and citation presentation
- side panels and history
- streaming and loading states
- tool invocation feedback
Do not blindly add a chat layout unless conversation is the primary task.

### Productivity and Collaboration
Useful references: Notion, Linear, Slack, Asana, Todoist.
Study:
- fast scanning
- keyboard-friendly interactions
- clear status and ownership
- compact controls
- progressive disclosure

### Commerce
Useful references: Shopify Admin, Stripe Checkout, Apple Store, modern direct-to-consumer storefronts.
Study:
- product comparison
- checkout focus
- price and variant hierarchy
- inventory and fulfillment states
- trust and error handling
Avoid unnecessary promotional clutter when the task is transactional.

### Mobile Apps
Useful references: Apple Human Interface Guidelines, Material Design, well-maintained native apps.
Study:
- touch targets
- bottom navigation vs top navigation
- modal and sheet patterns
- safe areas
- keyboard behavior
- native platform expectations

### Content and Publishing
Useful references: Medium, Substack, GitHub Docs, Stripe Docs, Apple documentation.
Study:
- readable measure
- heading rhythm
- navigation depth
- code and media presentation
- table of contents behavior

## Pattern References by UI Job

### Navigation
Consider: Linear, GitHub, Notion, Slack.
Use when studying sidebar hierarchy, workspace switching, nested navigation, compact global actions.

### Tables and Data Grids
Consider: GitHub, Stripe Dashboard, Shopify Admin, Linear.
Use when studying column priority, filters, row actions, bulk actions, pagination, status scanning.

### Settings
Consider: GitHub Settings, Slack Preferences, Stripe settings.
Use when studying section grouping, destructive zones, account vs workspace separation, form density.

### Forms
Consider: Stripe, GitHub, Shopify Admin.
Use when studying labels, help text, validation, save states, destructive actions, progressive sections.

### Authentication
Consider: GitHub, Vercel, Linear, Stripe.
Use when studying low-distraction sign-in, SSO options, recovery, error messages, security prompts.

### Search and Command
Consider: GitHub search, Linear command menu, Notion quick find.
Use when studying keyboard navigation, filters, recent items, empty results, result grouping.

### Chat and Messaging
Consider: ChatGPT, Claude, Slack.
Use when studying message rhythm, composer behavior, attachments, streaming, citations, tool results.

### Billing and Pricing
Consider: Stripe, Vercel, GitHub billing.
Use when studying plan comparison, usage, invoices, payment method status, upgrade paths.

### Onboarding
Consider: Linear, Notion, Vercel, Slack.
Use when studying progressive setup, useful defaults, skip paths, sample data, first-success moments.

### Empty States
Consider: GitHub, Linear, Notion, Stripe.
Study how the empty state explains what is missing and gives one useful next action without decorative filler.

### Errors and Recovery
Consider: GitHub, Stripe, Cloudflare Dashboard.
Study how the interface communicates impact, likely cause, retry options, and retained user input.

## Synthesis Rule

Never select a single reference and imitate it wholesale.
For substantial UI work, prefer a synthesis such as:

- one reference for information density
- one for interaction pattern
- one for state handling
- the current product for visual language

Example:

Project: analytics dashboard
- Linear for density and sidebar hierarchy
- Stripe for data explanation and tables
- GitHub for filters and row actions
- current project for typography, spacing, colors, radius, icons

The final result must feel like the current product, not like any named reference.
