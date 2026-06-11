# Developer Guidelines (CLAUDE.md)

This document provides architectural context, command references, and engineering constraints for Claude Code and development tools operating in this repository.

*Last updated: June 2026*

---

## Command Reference

Always use the following commands for development, building, and code quality:

* **Development Server:** `npm run dev` (Runs on port `3001`. Triggers `predev` to auto-convert HEIC images).
* **Production Build:** `npm run build` (Triggers `prebuild` to auto-convert HEIC images for SSG).
* **Production Start:** `npm run start` (Runs the compiled production build).
* **Linting & Quality:** `npm run lint` (Executes ESLint with Next.js `core-web-vitals` and strict TypeScript rules).

---

## Architecture & Stack Overview

This is a high-performance portfolio and blog website built on a modern frontend stack:

* **Framework:** Next.js 16 (App Router)
* **Core Libraries:** React 19, TypeScript
* **Styling & Animation:** Tailwind CSS v4, Framer Motion
* **Content Layer:** Markdown-powered Static Site Generation (SSG) for the blog.

### Import Path Mapping
* **Alias:** Always use the `~/` path alias to reference the `./src/` directory (e.g., `import { Button } from '~/components/ui/button'`). Do not use relative paths (`../../`).

### Repository Structure

```text
src/
├── app/                      # App Router routes and pages
│   ├── layout.tsx            # Global layout (Fonts, metadata, global UI wrapper)
│   └── page.tsx              # Single-page homepage composing all sections
├── components/
│   ├── sections/             # Ordered homepage sections (see sequence below)
│   └── ui/                   # Reusable atomic UI elements (Navbar, Footer, Button)
├── data/                     # Source of truth for portfolio content (TS Constants)
└── types/
    └── data.ts               # Shared TypeScript interfaces and type definitions
public/
└── profile/                  # Profile assets (Automated WebP conversion pipeline)