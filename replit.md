# Replit.md

## Overview

This is a static landing/promotional website for **@webhookos_bot**, a Telegram bot designed for community management, group tracking, and CTF/cybersecurity team coordination. The site serves as a marketing and informational portal with multiple pages showcasing the bot's features for both personal and corporate users.

The project is built as a pure frontend application using vanilla HTML, CSS, and JavaScript with Vite as the development/build tool. It features animated backgrounds, particle effects, multi-language support (English/Russian), and progressive web app (PWA) capabilities.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Technology Stack**: Vanilla HTML5, CSS3, and JavaScript (ES6+)
- **Build Tool**: Vite 5.x for development server and bundling
- **No Framework**: Deliberately framework-free for simplicity and performance

### Page Structure
- **Main Entry** (`index.html`): Primary landing page with slide-based presentation
- **Personal Section** (`/personal/`): Features for individual users (feed, groups, referrals)
- **Corporate Section** (`/corporate/`): Business-focused features
- **About Page** (`about.html`): Team and project information
- **404 Page** (`404.html`): Custom error page

### Visual Effects System
- **Canvas-based particle system**: Animated floating particles rendered via 2D canvas
- **Dynamic gradient backgrounds**: HSL color cycling animation for visual appeal
- **CSS Variables**: Theme support with light/dark mode using CSS custom properties

### Internationalization
- **Translation System**: JavaScript object-based translations (`translations.js`, `add-on.js`)
- **Supported Languages**: English (en), Russian (ru)
- **Storage**: LocalStorage for user preference persistence

### PWA Implementation
- **Service Worker** (`service-worker.js`): Cache-first strategy for offline support
- **Manifest** (`manifest.json`): App installation metadata
- **Install Prompt** (`serv.js`): Custom install button handling

### Security Measures
- Content Security Policy (CSP) headers via meta tags
- X-Frame-Options for clickjacking protection
- Strict Transport Security headers
- No-referrer policy

## External Dependencies

### Build Tools
- **Vite 5.4.8**: Development server and production bundler
- **esbuild**: Used internally by Vite for fast compilation

### External Resources (CDN-linked in HTML)
- **Google Fonts**: Poppins font family
- **Cloudflare CDNJS**: Potential script hosting (referenced in CSP)

### Third-Party Integrations
- **Telegram**: Primary integration target - the bot lives at `@webhookos_bot`
- **Social Media Meta Tags**: Open Graph (Facebook, LinkedIn) and Twitter Cards for sharing

### No Backend/Database
- This is a purely static site with no server-side components
- No database integration
- All data is either static or stored in browser localStorage