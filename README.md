# CodeSwitch

A code switcher landing page featuring background animations, a custom Prism syntax theme, and active toggle menu. Built as a portfolio and skills-building project.

**Live demo:** [make-it-decaf.vercel.app](https://make-it-decaf.vercel.app/)

## About

CodeSwitch is a landing page for a fictional API key authentication service (similar to [Unkey](https://unkey.dev/)). The page showcases SDK code examples across seven languages with tabbed switching, syntax highlighting via [Prism.js](https://prismjs.com/), and scroll-triggered footer animations.

Inspired by [thehashton/codeswitcher](https://github.com/thehashton/codeswitcher/) with changes for responsiveness and personal preference — primarily menu layout, padding adjustments for cross-device visuals, and color choices.

## Custom Prism Theme

None of the default Prism themes felt right for this build. Tried [G. Farhad's CodeMirror themes](https://github.com/FarhadG/code-mirror-themes) — starred for reference, but none were quite the fit either.

Used AI to pull colors from my personal website and generate a custom theme. Ultimately settled on a primarily Claude-inspired palette with off-white from my site, which also makes the SVG accent colors pop.

**TODO:** Download an official Prism theme stylesheet and make edits there rather than in `style.css`. Leaving as-is on GitHub for tinkering.

## Roadmap

This is currently a frontend-only portfolio piece. Long-term concept is to incrementally build it into a working API key authentication service — learning backend development along the way.

### Phase 1: Build a Simple REST API
Use Next.js API routes to create a basic CRUD API (e.g., a bookmarks/links service). No new tools — focus on request/response, HTTP methods, status codes, and JSON handling with the existing stack.

### Phase 2: Add a Database
Integrate a real database (either Firebase, or SQLite via Drizzle ORM or Prisma) so data persists between sessions. Focus: schemas, queries, and migrations.

### Phase 3: API Key Authentication
Generate API keys on signup, store hashed versions, and validate incoming requests via an `Authorization` header. This is the core concept the landing page already illustrates — now made real.

### Phase 4: Mini CodeSwitch Service
Extract the auth logic into a standalone service with endpoints for key creation, verification, and revocation. Add rate limiting and a usage dashboard. Connect the landing page to the real backend.

### Phase 5 (Stretch): Python + Linux
Rebuild the core verify endpoint in Python (FastAPI) and deploy on a Linux VPS to learn server administration, SSH, nginx, and systemd.

## Tech Stack

- HTML / CSS / JavaScript
- [Prism.js](https://prismjs.com/) for syntax highlighting
- Deployed on [Vercel](https://vercel.com/)