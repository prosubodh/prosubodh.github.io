# Tasks: Design Consistency Overhaul

## Phase 1: Global Style Polish
- [x] **[T1.1]** Update `style.css` variables: Add missing tokens if any, ensure light mode is fully consistent.
- [x] **[T1.2]** Fix Link Typography: Add explicit color rules for `a` tags containing headers (h1-h6) to use `var(--text-primary)`.
- [x] **[T1.3]** Refine Button Styles: Ensure hover states and transitions are identical across all button variants.

## Phase 2: Resume Integration
- [x] **[T2.1]** Update `resume.html` Head: Load Google Font "Outfit" and link `style.css`.
- [x] **[T2.2]** Body Structure: Add `.bg-mesh` and `.noise-overlay` to `resume.html` for ambient effects.
- [x] **[T2.3]** Section Refactoring: Wrap resume sections (Summary, Skills, Experience) in `.glass-card` for a premium look.
- [x] **[T2.4]** Theme Sync: Replace simple theme toggle with the SVG-based toggle from `index.html`.
- [x] **[T2.5]** Print Optimization: Ensure `@media print` in `style.css` handles the glassmorphism elements correctly (hides mesh, makes text black on white).

## Phase 3: Content Polish
- [x] **[T3.1]** Project Cards: Standardize the abstract graphics and fixed link inheritance.
- [x] **[T3.2]** Responsive Check: Ensure the new glass-card layout for the resume works well on mobile.

## Phase 4: Final Validation
- [x] **[T4.1]** Audit both pages for color contrast and accessibility.
- [x] **[T4.2]** Cross-browser check for glassmorphism support.
- [x] **[T4.3]** Cleanup: Remove legacy SCSS files and fix syntax issues.
