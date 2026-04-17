# Research: Portfolio Design Inconsistency

## Current State Analysis

### 1. File Structure & Styling Method
- **`index.html`**: Uses `style.css` which implements a modern "Glassmorphism" design system with CSS variables, the "Outfit" font, and ambient background effects.
- **`resume.html`**: Uses internal `<style>` tags with a completely independent set of rules. It uses "Helvetica Neue" and a very standard, "document-style" layout that clashes with the main site's premium feel.

### 2. Identified Inconsistencies
| Element | `index.html` | `resume.html` |
| :--- | :--- | :--- |
| **Typography** | Outfit (800 for headers) | Helvetica Neue |
| **Colors** | HSL/Hex based on CSS variables | Hardcoded Hex (#333, #2c3e50, #3b82f6) |
| **Background** | Animated Mesh + Glassmorphism | Solid White/Dark |
| **Buttons** | Rounded (9999px), subtle shadows | Slightly rounded (5px), solid blue |
| **Toggle** | SVG Icons (Sun/Moon) | Emoji (🌙) |

### 3. Visual Issues (from screenshots)
- **Project Titles**: In Image 3, the project titles (`GRC Enterprise Platform`, etc.) appear in a default-looking bright blue. This is likely due to them being inside an `<a>` tag without an explicit color override for the heading itself.
- **Resume Layout**: Image 1 shows a very basic header and a print button that doesn't follow the site's accent color (`#8b5cf6` vs `#3b82f6`).

## Design Recommendations
- **Unified Tokens**: Move all design tokens into `style.css` and use them in both files.
- **Shared Font**: Load "Outfit" in `resume.html`.
- **Component Parity**: Update the `resume.html` theme toggle and print button to match the portfolio's aesthetics.
- **Refined Project Cards**: Ensure `h3` inside `.project-card` always uses `var(--text-primary)`.
- **Premium Background**: Bring the ambient background mesh to the resume page for visual continuity.

## Refined Tech Stack
- **Core**: HTML/CSS (Vanilla)
- **Typography**: Google Fonts (Outfit)
- **Icons**: Lucide-style SVG (hardcoded for zero dependencies)
- **Animations**: CSS Keyframes + Intersection Observer
