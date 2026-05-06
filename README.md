# macer-park.github.io

Personal portfolio + retrospective. Built with Astro 5 + Tailwind 4.
Deployed to https://macer-park.github.io/ via GitHub Actions.

## Structure

```
src/
├── components/     # Header, Footer, MetricBadge, ProjectCard
├── consts.ts       # Site metadata, author, taglines, navigation
├── layouts/
│   └── BaseLayout.astro   # HTML shell + SEO meta + JSON-LD Person schema
├── pages/
│   ├── index.astro        # English landing
│   ├── codification.astro # Retrospective (en)
│   ├── now.astro          # Living signal (en)
│   ├── contact.astro
│   ├── projects/
│   │   ├── global-e.astro
│   │   ├── puzzle.astro
│   │   ├── toss.astro
│   │   └── ubiquoss.astro
│   └── ko/                # Korean mirror (index, codification, now, contact)
└── styles/
    └── global.css
```

## Commands

| Command           | Action                                            |
| :---------------- | :------------------------------------------------ |
| `npm install`     | Install dependencies                              |
| `npm run dev`     | Local dev server at `localhost:4321`              |
| `npm run build`   | Build static site to `./dist/`                    |
| `npm run preview` | Preview production build locally                  |

## Languages

- English (default at `/`)
- Korean (mirrored at `/ko/`)

## Deploy

Pushing to `main` triggers `.github/workflows/deploy.yml`, which uses
`withastro/action@v3` to build and deploy via `actions/deploy-pages@v4`.

In GitHub repo settings, ensure **Pages → Build and deployment → Source = GitHub Actions**.
