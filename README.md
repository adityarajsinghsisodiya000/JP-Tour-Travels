# ðŸŒ JP Tour & Travels

A modern **travel booking & tourism platform** built for Indian travel agencies. Curated tour packages, destination guides, vehicle rentals, photo gallery, travel blog and customer reviews â€” all in one fast Next.js application with a full admin CMS.

> âœ¨ **Live demo:** [https://baneshwari.gt.tc/](https://baneshwari.gt.tc/)

---

## âœ¨ Features

### Public website
- ðŸ  **Home page** â€” hero, stats, package showcase, gallery preview, review carousel
- ðŸŽ’ **Tour Packages** â€” searchable & filterable list (duration, price) with rich detail pages
- ðŸ—ºï¸ **Destinations** â€” curated destination guides with detail pages
- ðŸš— **Vehicle Fleet** â€” per-km pricing and WhatsApp-first booking flow
- ðŸ–¼ï¸ **Gallery** â€” category-filtered photo gallery (Cloudinary)
- ðŸ“ **Travel Blog** â€” articles with detail pages
- â­ **Reviews** â€” rating summary & testimonials
- ðŸ“ž **Contact & FAQ** â€” validated contact form + WhatsApp deep links, FAQ accordion
- ðŸŒ“ **Dark mode** with page transitions & GSAP animations

### Admin CMS (`/admin`)
- ðŸ” Supabase auth with middleware-protected routes
- ðŸ“Š Dashboard with stats & data tables
- âœï¸ Packages & Destinations CRUD
- ðŸ–¼ï¸ Media library with drag-drop uploader
- ðŸ  Homepage CMS & SEO editor
- âš™ï¸ Site settings (general / WhatsApp / social)

### Backend & APIs
- REST API routes for **contact, destinations, gallery, packages, vehicles** with zod validation
- Supabase Postgres schema (9 tables) with RLS & public-read policies
- Soft-delete pattern, slug uniqueness checks, pagination
- SEO: `sitemap.xml`, `robots.txt`, manifest

---

## ðŸ› ï¸ Tech Stack

| Layer | Tech |
|---|---|
| Frontend | Next.js 16 Â· React 19 Â· TypeScript 5 Â· Tailwind CSS 4 Â· shadcn/ui |
| Backend | Next.js API routes Â· Supabase (Postgres + Auth + Storage) |
| Media | Cloudinary (image uploads & transformations) |
| UI/UX | framer-motion Â· GSAP Â· lucide-react Â· next-themes Â· sonner |
| Validation | zod 4 |

---

## ðŸš€ Getting Started

```bash
# 1. Install dependencies
npm install

# 2. Set up environment variables
#    Copy .env.example content into .env.local and fill in your Supabase & Cloudinary keys
#    (NEXT_PUBLIC_SUPABASE_URL, NEXT_PUBLIC_SUPABASE_ANON_KEY, NEXT_PUBLIC_CLOUDINARY_CLOUD_NAME)

# 3. Run migrations (apply the schema to your Supabase project)
#    supabase db push

# 4. Start the dev server
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

---

## ðŸ“ Project Structure

```
src/
â”œâ”€â”€ app/
â”‚   â”œâ”€â”€ (main)/            # Public site (home, packages, destinations, blog, ...)
â”‚   â”œâ”€â”€ (admin)/           # Admin CMS (/admin: dashboard, CRUD, media, SEO, settings)
â”‚   â””â”€â”€ api/               # REST API routes
â”œâ”€â”€ components/
â”‚   â”œâ”€â”€ ui/                # Reusable UI (shadcn)
â”‚   â”œâ”€â”€ shared/            # Navbar, footer, WhatsApp button, breadcrumbs
â”‚   â”œâ”€â”€ home/ packages/ destinations/ gallery/ blog/ reviews/ admin/
â”œâ”€â”€ lib/
â”‚   â”œâ”€â”€ services/          # Data services (packages, destinations, vehicles, whatsapp)
â”‚   â”œâ”€â”€ supabase/          # Supabase client
â”‚   â””â”€â”€ cloudinary/        # Cloudinary uploads
â”œâ”€â”€ hooks/                 # Custom hooks
â””â”€â”€ types/                 # TypeScript types matching the DB schema
```

---

## ðŸ“„ License

This project is a private/commercial codebase. Contact the owner for usage terms.

---

**Built with â¤ï¸ by [Aditya Raj Singh Sisodiya](https://github.com/adityarajsinghsisodiya000)**