# Trip Planner Plugin

Interactive travel planning toolkit for Claude. Research destinations, plan itineraries, generate HTML travel guides, and deploy as live websites.

## Skills

| Skill | Description |
|-------|-------------|
| **trip-planner** | Main orchestrator -- conversational trip planning from research to confirmation (Phases 0-4.5) |
| **travel-collector** | Extract and organize travel research from URLs, screenshots, text notes into structured JSON |
| **flight-intelligence** | Flight price research, seasonality analysis, buy-now-or-wait recommendations |
| **trip-html-generator** | Generate interactive HTML travel guide with maps, calendar, budget tracker, and more |
| **ui-style** | 30 design styles (cyberpunk, swiss minimalist, neo-brutalism, etc.) for the HTML output |
| **trip-deployer** | Deploy the generated HTML to GitHub Pages, Netlify, Vercel, or Cloudflare Pages |

## Workflow

```
travel-collector          (collect research from links/screenshots)
       |
       v
trip-planner              (orchestrate planning: gather -> recommend -> route -> research)
  |         |
  |         v
  |    flight-intelligence (flight price analysis if not booked)
  |
  v
ui-style                  (pick a visual style)
  |
  v
trip-html-generator       (generate the interactive HTML travel guide)
  |
  v
trip-deployer             (publish as a live website)
```

## Install

Upload the `.plugin` file in Claude Desktop, or add this repo as a marketplace:

```
owner/repo
```
