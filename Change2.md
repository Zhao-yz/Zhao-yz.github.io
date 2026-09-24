# Change 2: Add light and dark themes

## Goal

Let visitors read the site comfortably in light or dark mode, and fix two small alignment issues in the header and footer.

## Plan

1. Add a dark color theme next to the existing light theme using CSS custom properties, with accessible contrast in both themes.
2. Follow the visitor's system setting by default (prefers-color-scheme).
3. Add a small, accessible theme toggle button in the header that switches between light and dark and remembers the choice in localStorage; apply the saved theme before first paint so there is no flash.
4. Fix alignment: all navigation items sit on the same baseline (Home is currently higher than the others), and the footer Email and LinkedIn links sit on the same line.
5. Keep all page content and page structure unchanged.

## Done when

The toggle works on every page, the choice persists across pages and reloads, both themes keep accessible contrast, and the header and footer look aligned at 375px and 1280px widths.