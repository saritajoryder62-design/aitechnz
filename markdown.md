# Independent AB Technician Project Documentation

## Project Refactoring (CSS Consolidation)

This project has been refactored to improve maintainability and performance by moving internal and inline CSS into a separate stylesheet.

### Changes Made:
1.  **CSS Consolidation**: All `<style>` blocks and inline `style` attributes from `index.html`, `booking.html`, and `thank-you.html` have been moved to `css/style.css`.
2.  **CSS Fixes**: 
    - Resolved a selector mismatch in `thank-you.html` where `.home-btn` was defined but `.home-link` was used.
    - Standardized `:root` variables across all pages for consistent branding.
    - Improved layout consistency by ensuring `box-sizing: border-box` is applied to all form elements.
    - Fixed a specificity issue where global label styles were breaking radio button alignment.
3.  **HTML Cleanup**: Removed cluttered internal styles and replaced them with meaningful class names (e.g., `.badge-pill`, `.map-pin`).
4.  **Best Practices**: Moved CSS to external files to leverage browser caching and improve code readability.

### File Structure:
- `index.html`: Main landing page (Technician profile & service area).
- `booking.html`: Farm information and booking enquiry form.
- `thank-you.html`: Confirmation page after form submission.
- `css/style.css`: Unified stylesheet for the entire application.
- `README.md`: Getting started guide and tech stack details.

### How to Deploy:
1. **Initialize if needed**: `git init`
2. **Add Remote**: `git remote add origin https://github.com/saritajoryder62-design/aitechnz.git`
3. **Commit all changes**:
   `git add . && git commit -m "Refactor: Move CSS to separate file and fix style errors"`
4. **Push to GitHub**:
   `git push -u origin main`
5. **Live Deployment**: Netlify will automatically trigger a rebuild at:
   https://astonishing-swan-59a350.netlify.app/