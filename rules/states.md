# UI State Rules

For each feature, list relevant states before completion.

## Data Regions

Consider:
- loading
- success
- empty
- error
- stale
- partial
- permission denied
- offline/unavailable

## Controls

Consider:
- default
- hover
- focus-visible
- active/pressed
- disabled
- selected
- validation error
- success

## Requirements

- Loading state should preserve expected layout when practical.
- Empty state should explain the condition and next useful action.
- Error state should identify the problem and recovery path when possible.
- Disabled state should not be the only way to communicate a requirement.
- Success feedback should be proportionate to the action.
- Destructive operations should support prevention or recovery appropriate to their impact.
