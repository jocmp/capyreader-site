# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

| Command | Description |
|---------|-------------|
| `npm run dev` | Start development server at localhost:4321 |
| `npm run build` | Build production site to ./dist/ |
| `npm run preview` | Preview build locally before deploying |
| `npm run astro ...` | Run Astro CLI commands (e.g., `astro add`, `astro check`) |

## Architecture

This is an Astro static site for Capy Reader, an Android RSS reader app. The architecture follows Astro's standard patterns:

- **Layout System**: Single base layout (`Layout.astro`) provides HTML structure and global styles
- **Component-Based**: Main content in `HomeView.astro` component with hero section for app marketing
- **Asset Management**: Static assets in `src/assets/` (hero image, app store badges) and `public/` (favicon)
- **Styling**: Component-scoped CSS within .astro files, extensive commented-out styles in HomeView suggest work-in-progress

The site appears to be transitioning from Hugo (evident from removed .hugo_build.lock and git history) to Astro as the static site generator.

## Project Structure

```
src/
├── assets/          # Static assets (images, etc.)
├── components/      # Reusable Astro components
├── layouts/         # Page layouts
└── pages/           # Route pages (index.astro = homepage)
```

## Development Notes

- Uses Astro's strict TypeScript configuration
- Single-page site focused on app promotion
- Responsive design with mobile-first approach (evident in extensive media queries)
- Currently has extensive commented-out CSS in HomeView component