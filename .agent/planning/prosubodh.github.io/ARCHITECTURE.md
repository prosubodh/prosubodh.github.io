# Architecture: Unified Portfolio Design

## Design System
We will consolidate the design tokens into `style.css` and treat it as the "Source of Truth" for the entire portfolio.

### 1. Variables Strategy
- **Base Colors**: `--bg-base`, `--bg-surface`, `--text-primary`, `--text-secondary`.
- **Accents**: `--accent-primary` (Purple), `--accent-secondary` (Cyan).
- **Glassmorphism**: `--glass-bg`, `--glass-border`, `--glass-highlight`, `--glass-shadow`.

### 2. Component Structure
- **Global Header**: Shared logic for theme toggling.
- **Glass Card**: Standard container for project items, timeline entries, and resume sections.
- **Button System**:
  - `.btn.primary-btn`: Solid primary accent or text color.
  - `.btn.secondary-btn`: Glass/Border style.

## Structural Changes

### `style.css` Updates
- Explicitly style headings inside links to prevent browser default blue.
- Add utility for "Print-Friendly" sections to support `resume.html`.

### `resume.html` Refactoring
- Link to `style.css`.
- Remove internal `<style>` block.
- Use `.glass-card` for resume sections (Summary, Experience, Education).
- Implement the same ambient background mesh as `index.html`.
- Match theme toggle icons and behavior.

### `index.html` Polish
- Ensure all CTA buttons use the same design pattern.
- Fix project card heading inheritance.
