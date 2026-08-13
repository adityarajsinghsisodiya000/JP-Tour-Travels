# 🌍 JP Tour & Travels

A modern **travel booking & tourism platform** built for Indian travel agencies. Curated tour packages, destination guides, vehicle rentals, photo gallery, travel blog and customer reviews — all in one fast Next.js application with a full admin CMS.

> ✨ **Live demo:** [https://baneshwari.gt.tc/](https://baneshwari.gt.tc/)

---

## ✨ Features

### Public website
- 🏠 **Home page** — hero, stats, package showcase, gallery preview, review carousel
- 🎒 **Tour Packages** — searchable & filterable list (duration, price) with rich detail pages
- 🗺️ **Destinations** — curated destination guides with detail pages
- 🚗 **Vehicle Fleet** — per-km pricing and WhatsApp-first booking flow
- 🖼️ **Gallery** — category-filtered photo gallery (Cloudinary)
- 📝 **Travel Blog** — articles with detail pages
- ⭐ **Reviews** — rating summary & testimonials
- 📞 **Contact & FAQ** — validated contact form + WhatsApp deep links, FAQ accordion
- 🌓 **Dark mode** with page transitions & GSAP animations

### Admin CMS (`/admin`)
- 🔐 Supabase auth with middleware-protected routes
- 📊 Dashboard with stats & data tables
- ✏️ Packages & Destinations CRUD
- 🖼️ Media library with drag-drop uploader
- 🏠 Homepage CMS & SEO editor
- ⚙️ Site settings (general / WhatsApp / social)

### Backend & APIs
- REST API routes for **contact, destinations, gallery, packages, vehicles** with zod validation
- Supabase Postgres schema (9 tables) with RLS & public-read policies
- Soft-delete pattern, slug uniqueness checks, pagination
- SEO: `sitemap.xml`, `robots.txt`, manifest

---

## 🛠️ Tech Stack

| Layer | Tech |
|---|---|
| Frontend | Next.js 16 · React 19 · TypeScript 5 · Tailwind CSS 4 · shadcn/ui |
| Backend | Next.js API routes · Supabase (Postgres + Auth + Storage) |
| Media | Cloudinary (image uploads & transformations) |
| UI/UX | framer-motion · GSAP · lucide-react · next-themes · sonner |
| Validation | zod 4 |

---

## 🚀 Getting Started

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

## 📁 Project Structure

```
src/
├── app/
│   ├── (main)/            # Public site (home, packages, destinations, blog, ...)
│   ├── (admin)/           # Admin CMS (/admin: dashboard, CRUD, media, SEO, settings)
│   └── api/               # REST API routes
├── components/
│   ├── ui/                # Reusable UI (shadcn)
│   ├── shared/            # Navbar, footer, WhatsApp button, breadcrumbs
│   ├── home/ packages/ destinations/ gallery/ blog/ reviews/ admin/
├── lib/
│   ├── services/          # Data services (packages, destinations, vehicles, whatsapp)
│   ├── supabase/          # Supabase client
│   └── cloudinary/        # Cloudinary uploads
├── hooks/                 # Custom hooks
└── types/                 # TypeScript types matching the DB schema
```

---

## 📄 License

This project is a private/commercial codebase. Contact the owner for usage terms.

---

**Built with ❤️ by [Aditya Raj Singh Sisodiya](https://github.com/adityarajsinghsisodiya000)**