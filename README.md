# Team Yanke Bionics — 28×28 Campaign Dashboard

A live, single-file command center for Team Yanke Bionics' run in the **28×28 Mobility Challenge** (So Every BODY Can Move). It reads the device clock, counts down to the next post, and tracks engagement and fundraising across the campaign.

**Live page:** https://yankedecks.github.io/28x28-dashboard/
**Team page:** https://charity.pledgeit.org/t/cdyg9rpsjh

---

## What it does

- **Overview** — total engagement, posts logged, average per post, and dollars raised at a glance; a live countdown to the next post that flips to **DUE NOW** on the day; an engagement-over-time chart; and auto-generated insights (top post, strongest channel, video vs. static).
- **Engagement** — pick any post, paste each platform's link, and enter likes / comments / shares. Builds a platform breakdown, an average-by-post-type chart, and ranked post cards that link straight out to the live posts.
- **Schedule** — the full teaser + 28-day plan with done / next / due status, copy-caption, and mark-posted on every item.
- **Fundraising** — raised vs. goal with a progress bar, a "beat last year ($7,710)" marker, and a raised-over-time curve you build by logging totals.

Everything you enter saves in your browser and persists on this page.

---

## Editing

All campaign data lives in the **`CONFIG`** block at the top of the `<script>` in `index.html` — dates, captions, the team link, the fundraising goal, and the July post rotation. Change values there and re-commit; no build step.

```
const CONFIG = {
  teamUrl: '…',        // team donation page
  goalDefault: 8000,   // starting fundraising goal
  launch: '2026-07-01',
  finish: '2026-07-28',
  teasers: [ … ],      // the three teaser posts + captions
  rotation: [ … ],     // July daily post types + captions
};
```

---

## Notes

- Charts use Chart.js from a CDN, so the live page needs a normal internet connection.
- Times are local to the viewer's device (Eastern for the team).
- Single file, no dependencies to install — just `index.html`.

Built for Team Yanke Bionics · Akron, Ohio · *Accept No Limitations.*
