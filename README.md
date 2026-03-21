# GA Dashboards

Internal dashboards for Gastroenterology Associates, P.A.

## Structure

```
ga-dashboards/
├── staff/              # Staff Dashboard (base-index.html)
│   ├── index.html
│   └── auth-redirect.html
├── it/                 # IT Dashboard (it-index.html)
│   ├── index.html
│   └── auth-redirect.html
├── provider/           # Provider Dashboard (provider-index.html)
│   ├── index.html
│   └── auth-redirect.html
└── shared/             # Assets shared across all dashboards
    ├── GA_logo_transparent.png
    ├── icon-192.png
    ├── icon-512.png
    ├── manifest.json
    └── service-worker.js
```

## Netlify Deployment

Each dashboard is deployed as its own Netlify site. Set the **Publish directory**
for each site to its corresponding subfolder:

| Dashboard | Netlify Publish Directory |
|-----------|--------------------------|
| Staff     | `staff`                  |
| IT        | `it`                     |
| Provider  | `provider`               |

The shared assets (logo, icons, manifest, service worker) should be copied into
each site's publish directory alongside `index.html` before deploying.

## Workflow

**Before starting work:**
```bash
git pull
```

**After making changes:**
```bash
git add .
git commit -m "Brief description of what changed"
git push
```
