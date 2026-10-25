# Sumit Tripathy — Portfolio

> **Live Portfolio:** [https://sumittripathy.netlify.app](https://sumittripathy.netlify.app)

Explore my portfolio to see my projects, technical skills, professional experience, and contact details.

A responsive React portfolio built with Vite. Profile, project, and experience content is stored locally in `src/data`, so the site ships as static files and does not need Spring Boot or a database.

## Repository structure

```text
public/
├── _redirects                      # SPA route fallback for Netlify/Cloudflare Pages
├── images/                         # Illustrative project previews for case studies
├── SUMIT_TRIPATHY_FULLSTACK.pdf    # Downloadable resume
└── sumit-mark.svg                  # Portfolio favicon
src/
├── App.jsx                         # Routes and hash-scroll handling
├── App.css                         # Homepage, case study, and responsive styles
├── main.jsx                        # React entry point and BrowserRouter
├── data/
│   ├── profile.js                  # Profile, education, and experience content
│   └── projects.js                 # Case study copy, metrics, and technologies
├── layout/
│   ├── header/SiteHeader.jsx       # Brand and section navigation
│   └── footer/SiteFooter.jsx       # Footer links and profile summary
├── pages/
│   ├── HomePage.jsx                # Homepage section composition
│   └── ProjectPage.jsx             # Click-through project detail pages
├── project/FeatureCard.jsx         # Reusable project card
└── sections/
    ├── HeroSection.jsx             # Intro and verification flow visual
    ├── ImpactStrip.jsx             # Resume metrics
    ├── FeaturedWork.jsx            # Project cards and links
    ├── ExperienceTimeline.jsx      # Work history
    ├── Toolkit.jsx                 # Skills grouped by area
    ├── AboutEducation.jsx          # Education details
    └── ContactSection.jsx          # Contact call-to-action
```

## Run locally

Requires Node.js 20.19+ (or 22.12+) and npm.

```bash
npm ci
npm run dev
```

Create a production build and preview it locally:

```bash
npm run build
npm run preview
```

## Deploy

The production build is written to `dist/`.

- **Vercel:** import this repository; use `npm run build` as the build command and `dist` as the output directory. `vercel.json` includes the client-side route rewrite.
- **Netlify or Cloudflare Pages:** use `npm run build` as the build command and `dist` as the publish directory. `netlify.toml` and `public/_redirects` include the client-side route fallback.

The resume preview and download use `public/SUMIT_TRIPATHY_FULLSTACK.pdf`, as configured in `src/data/profile.js`. Replace that file to publish an updated resume without changing its URL. Case study previews are illustrative interface concepts, not production screenshots. The order rows in the project preview are illustrative sample data.
