# lyink

Open-source "link in bio" page. Zero dependencies, zero build tools, pure HTML/CSS/JS.

Deploy your own links page in 30 seconds.

## Features

- **Zero dependencies** — No npm, no frameworks, no build step
- **Visual editor** — Add links, drag & drop reorder, live preview, export
- **3 themes** — Glass (blur), Solid, Minimal
- **18+ icons** — WhatsApp, Instagram, Telegram, X, GitHub, LinkedIn, YouTube, TikTok, Discord, Spotify, and more
- **Grid sections** — Catalog-style grid layouts (like WhatsApp catalogs)
- **i18n** — Multi-language support with auto-detection + RTL
- **Mobile-first** — Responsive, safe-area aware, touch optimized
- **SEO** — Dynamic meta tags, Open Graph
- **Self-hosted** — Your data, your page, no tracking

## Quick Start

### Option 1: Edit config.json

1. Fork this repo
2. Edit `config.json` with your links
3. Deploy to GitHub Pages / Vercel / Netlify

### Option 2: Use the visual editor

1. Open `editor.html` in your browser
2. Add your links, pick a theme, set your avatar
3. Click **Export JSON** or **Export HTML**

## Deploy

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/reputasyon/lyink)
[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/reputasyon/lyink)

**GitHub Pages:** Go to Settings → Pages → Source: main branch → Save.

## Config

All configuration is in `config.json`:

```json
{
  "name": "Your Name",
  "bio": "Short bio",
  "avatar": "assets/avatar.png",
  "background": {
    "type": "image",
    "src": "assets/bg.gif",
    "overlay": 0.55
  },
  "theme": {
    "style": "glass",
    "radius": 16
  },
  "links": [
    {
      "title": "Instagram",
      "url": "https://instagram.com/you",
      "icon": "instagram"
    }
  ],
  "sections": [
    {
      "title": "My Catalog",
      "type": "grid",
      "columns": 2,
      "items": [
        {
          "title": "Item",
          "subtitle": "Description",
          "url": "https://...",
          "icon": "image"
        }
      ]
    }
  ],
  "seo": {
    "title": "Page Title",
    "description": "Page description"
  }
}
```

### Available Icons

`whatsapp` `instagram` `telegram` `twitter` `github` `linkedin` `youtube` `tiktok` `discord` `spotify` `threads` `snapchat` `email` `website` `phone` `location` `send` `image` `link`

### Themes

| Theme | Description |
|-------|-------------|
| `glass` | Frosted glass cards with backdrop blur |
| `solid` | Opaque dark cards |
| `minimal` | Borderless, clean text links |

### Background Types

| Type | Fields |
|------|--------|
| `image` | `src`, `overlay` (0-1) |
| `color` | `color` (hex) |
| `gradient` | `gradient` (CSS gradient string) |

## Project Structure

```
lyink/
├── index.html      # Main page — reads config.json
├── editor.html     # Visual editor with live preview
├── config.json     # Your configuration
├── icons.svg       # SVG icon sprite (18+ platforms)
├── assets/         # Your images (avatar, background)
├── README.md
└── LICENSE
```

## License

MIT
