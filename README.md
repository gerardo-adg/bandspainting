# B&S Painting Inc — Quiz Funnel

A 3-step quiz funnel built for Meta ads traffic. It's a single static page with no build step.

## Setup
1. **Logo:** add the logo at `assets/logo.png`. A text logo shows until then.
2. **Config:** edit `FUNNEL_CONFIG` at the top of `index.html`: service area, phone, Meta Pixel ID and an optional webhook URL.
3. **Brand colors:** change `--accent` and `--bg-1` / `--bg-2` in `:root`.
4. **Deploy:** connect this repo to Netlify. Leads come in under **Netlify → Forms → painting-quote**. You can also send them to GoHighLevel or Zapier through `webhookUrl`.

## Tracking
- `PageView` fires on load and `Lead` fires on submit (once the Pixel ID is set).
- UTM parameters and `fbclid` are saved with each lead.
