# PSK Services — Event Booking Website

A complete event booking website for an event services business. Browse services, read the blog, check references, and complete a multi-step booking flow — all client-side. Built with Vite, React, TypeScript, Tailwind CSS, and shadcn/ui.

## Features

- **Home page** — hero, service highlights, testimonials, call-to-action sections
- **Services page** — event service catalog with details
- **Multi-step booking flow** — guided booking form with step progress
- **Blog** — article listing + detail pages (`/blog`, `/blog/:id`)
- **References page** — client references / portfolio showcase
- **Shared layout** — navbar, footer, 404 page
- **Responsive design** — mobile-first Tailwind layout with full shadcn/ui kit
- **Toasts & tooltips** — Sonner + Radix-based notifications

## Tech Stack

- **Framework:** React 18 + TypeScript + Vite
- **Styling:** Tailwind CSS + shadcn/ui (Radix primitives)
- **Routing:** React Router (BrowserRouter)
- **Data fetching:** TanStack Query
- **Forms:** React Hook Form + Zod validation

## Quick Start

```bash
npm install --legacy-peer-deps
npm run dev        # start dev server
npm run build      # production build -> dist/
npm run preview    # preview the production build
```

Requirements: Node.js 18+.

## Project Structure

```
├── index.html
├── public/                  # static assets
├── src/
│   ├── App.tsx              # router + providers (QueryClient, Tooltip, Toaster)
│   ├── main.tsx             # entry point
│   ├── pages/
│   │   ├── Index.tsx        # home
│   │   ├── Services.tsx     # service catalog
│   │   ├── Booking.tsx      # multi-step booking flow
│   │   ├── Blog.tsx         # blog listing
│   │   ├── BlogDetail.tsx   # blog article
│   │   ├── References.tsx   # client references
│   │   └── NotFound.tsx     # 404
│   ├── components/
│   │   ├── Navbar.tsx, Footer.tsx, ...
│   │   └── ui/              # shadcn/ui components
├── tailwind.config.ts
├── vite.config.ts
└── tsconfig.json
```

## Deploy

Static site — deploy the `dist/` folder to any static host:

```bash
npm run build
# then deploy dist/ to Cloudflare Pages, Netlify, or GitHub Pages
```

No environment variables required. Because the app uses `BrowserRouter`, static hosts should rewrite all routes to `index.html` (a `_redirects` / `/* /index.html 200` rule) so deep links like `/booking` and `/blog/:id` work.

## License

MIT — free to use and adapt.

---

*Built by [Girish Lade](https://ladestack.in) — explore more open-source tools and products at [ladestack.in](https://ladestack.in).*
