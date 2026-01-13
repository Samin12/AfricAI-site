# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

AfricAI is a static event website for "The Creator Retreat" - an AI mastermind event in Cape Town, South Africa (Feb 2-7, 2026). It's a single-page application built with pure HTML and Tailwind CSS.

## Development Commands

```bash
# Start local development server (runs on port 3000)
npm start

# Health check endpoint
curl http://localhost:3000/health
```

## Architecture

**Stack**: Pure HTML5 + Tailwind CSS (CDN) + Express.js for static serving

**Key Files**:
- `index.html` - Complete single-page application (all content and styling)
- `server.js` - Express server that serves static files and handles routing
- `assets/AfricAI/` - Profile images for speakers/founders

**No Build Process**: Tailwind CSS is loaded via CDN (`cdn.tailwindcss.com`), no transpilation or bundling required.

## Design Conventions

- **Colors**: Black background (#000) with orange accents (Tailwind `orange-500` / #f97316)
- **Typography**: Inter font as primary (400-800 weights)
- **Styling**: All via inline Tailwind utility classes
- **Animations**: Custom CSS for scrolling marquees (vertical and horizontal), hover effects, and button glow

## Deployment

Configured for both Vercel and Railway:
- `vercel.json` - Vercel configuration
- `railway.json` + `.nixpacks` - Railway configuration with Node.js 18.x
