# B&S Painting Inc — Quiz Funnel

A 3-step quiz funnel for Meta ads traffic, built with [Astro](https://astro.build). It outputs a fast static site.

## Edit the funnel
Everything you'd normally change is in **`src/site.config.ts`**: business name, service area, phone, Meta Pixel ID, webhook URL and trust points.

| What | Where |
|---|---|
| Services, questions and answers | `src/components/Quiz.astro` |
| Headline, hero and "How it works" | `src/pages/index.astro` |
| Brand colors and fonts | `src/layouts/Base.astro` (`:root`) |
| Hero photo | `src/assets/photos/hero.jpg` (Unsplash license, free for commercial use) |
| Logo | `src/assets/logo.png` |

## Run locally
```bash
npm install
npm run dev
```

## Deploy (Netlify)
Connect this repo in Netlify. `netlify.toml` already sets the build command (`npm run build`) and the publish folder (`dist`).
Leads show up under **Netlify → Forms → painting-quote**. Turn on form notifications there to get email alerts.
To send leads to GoHighLevel or Zapier as well, set `webhookUrl`.

## Tracking
- Meta Pixel `PageView` fires on load and `Lead` fires on submit (once `metaPixelId` is set).
- UTM parameters and `fbclid` are saved with each lead.
