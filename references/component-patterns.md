# Component Pattern Guide

Use this guide to choose structure before styling.

## Sidebar
Use when the product has several stable destinations or nested workspace navigation.
Avoid when the experience has only a few top-level destinations.
Check:
- active state is obvious
- labels remain readable
- collapse behavior is intentional
- mobile replacement is designed
- secondary controls do not compete with primary navigation

## Top Navigation
Use when there are few global destinations or when horizontal space is appropriate.
Avoid pairing it with a redundant sidebar that repeats the same routes.

## Cards
Use for meaningful containment, independent objects, or scannable repeated entities.
Do not use cards as the default wrapper for every section.
Prefer open layout, dividers, alignment, and spacing when those are enough.

## Tables
Use for comparison across repeated records and columns.
Provide:
- clear headers
- useful alignment
- responsive strategy
- row selection when needed
- bulk actions when needed
- loading skeleton or progress
- empty and error states
- sorting and filters only when useful

## Lists
Use when order and scanning matter more than column comparison.
Keep metadata hierarchy stable between rows.

## Forms
Group by user intent, not by arbitrary card count.
Use clear labels and nearby validation.
Preserve user input after recoverable errors.

## Dialogs
Use for short focused tasks or confirmations.
Do not place large multi-step workflows in narrow dialogs.

## Drawers and Sheets
Use for contextual secondary tasks that should not fully replace the current page.
Design keyboard focus and mobile behavior.

## Tabs
Use for peer sections within the same context.
Do not use tabs for unrelated global navigation.
Avoid too many tabs when a list or sidebar is clearer.

## Accordions
Use for optional detail or FAQ-like content.
Do not hide critical workflow information by default.

## Toasts
Use for brief confirmation or non-blocking feedback.
Do not use toast messages as the only location for important error recovery instructions.

## Badges and Pills
Use for compact status, category, or filter state.
Avoid turning ordinary labels and buttons into pills by default.

## Charts
Use only when a visual pattern, trend, distribution, or comparison is easier to understand graphically.
Always provide meaningful labels, units, time ranges, and accessible alternatives where appropriate.
