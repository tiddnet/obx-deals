# obx-deals

Static frontend for [obx.deals](https://obx.deals) — OBX vacation rental deal aggregator and verified view badge program.

Hosted on GitHub Pages (CNAME: obx.deals). Deployed automatically on push to `main`.

## Pages

| File | URL | Purpose |
|---|---|---|
| `index.html` | obx.deals | Daily deal listings (regenerated nightly) |
| `about.html` | obx.deals/about | Our Story |
| `privacy.html` | obx.deals/privacy | Privacy policy + contact form |
| `view/*.html` | obx.deals/view/* | 50 static verified-view badge pages |

## How content gets here

This repo is **write-only from rental-intel**. Do not edit `index.html` directly — it is overwritten nightly by the deploy pipeline.

```
rental-intel/scripts/generate_deal_posts.py  →  index.html
rental-intel/scripts/deploy_obx_deals.sh     →  git commit + push (runs 6:15am daily)
```

`about.html`, `privacy.html`, and `view/` pages are edited directly in this repo.

## Related repos

| Repo | Site | Purpose |
|---|---|---|
| [rental-intel](https://github.com/tiddnet/rental-intel) *(private)* | — | Data pipeline, scrapers, Lambda infra, deploy scripts |
| [obx-search](https://github.com/tiddnet/obx-search) | search.obx.deals | Consumer property search |
| [obx-owners](https://github.com/tiddnet/obx-owners) | owners.obx.deals | Owner Hub (Auth0 login required) |

See `rental-intel/README.md` for the full system architecture, data flow, and AWS infrastructure.
</content>
</invoke>