# 🌿 Rutas con Niños

**Rutas con Niños** is a mobile-first React + TypeScript web app designed to help families discover child-friendly hiking trails and outdoor activities. The app offers interactive trail maps, a blog-style inspiration section, a calendar of family events, and a contact form — all tailored for parents exploring nature with kids.

---

## 🧭 Features

- 🏞️ **Home Page** – Welcoming carousel and introductory text about the project
- 🗺️ **Map Page** – Interactive Leaflet map with 5 preloaded trails from Wikiloc
- 📍 **Trail Cards** – Tap a card to locate the trail on the map, and tap a map marker to highlight the related card
- 💡 **Inspiration Page** – Blog-style layout for tips, tricks, and pinned family-friendly articles
- 📅 **Calendar Page** – Event calendar with automatic hiding of expired events
- 📬 **Contact Page** – Contact form and social media links to connect with the community

---

## ⚙️ Built With

- **React + TypeScript** – Component-based UI with strong typing
- **React Router** – Route-based navigation
- **Leaflet** – Interactive maps for exploring trails
- **Plain CSS (Mobile-First)** – Simple, scalable styling strategy
- **Modular Architecture** – Organized using a feature-first folder structure

---

## 📁 Project Structure

src/
│
├── assets/ # Images, icons, and static assets
│ └── images/
│
├── components/ # Reusable UI components
│ ├── Header.tsx
│ ├── Header.css
│ ├── Footer.tsx
│ ├── Footer.css
│ ├── Button.tsx
│ ├── Button.css
│ ├── Carousel.tsx
│ └── Carousel.css
│
├── features/ # Feature folders (by domain)
│ ├── trails/ # Trails map and interactive cards
│ │ ├── components/
│ │ │ ├── TrailCard.tsx
│ │ │ ├── TrailCard.css
│ │ │ ├── TrailMap.tsx
│ │ │ └── TrailMap.css
│ │ ├── hooks/
│ │ │ └── useSelectedTrail.ts
│ │ ├── services/
│ │ │ └── trailApi.ts
│ │ ├── trailTypes.ts
│ │ └── trailsData.ts # Static trail data (5 Wikiloc trails)
│ │
│ ├── inspiration/ # Blog-style tips & pinned posts
│ │ ├── components/
│ │ │ └── BlogPost.tsx
│ │ │ └── BlogPost.css
│ │ └── services/
│ │ └── inspirationApi.ts
│ │
│ ├── calendar/ # Event calendar with expiry
│ │ ├── components/
│ │ │ └── Calendar.tsx
│ │ │ └── Calendar.css
│ │ ├── services/
│ │ │ └── calendarApi.ts
│ │ └── utils/
│ │ └── filterExpiredEvents.ts
│ │
│ └── contact/ # Contact form and social links
│ ├── components/
│ │ ├── ContactForm.tsx
│ │ ├── ContactForm.css
│ │ ├── SocialLinks.tsx
│ │ └── SocialLinks.css
│ └── services/
│ └── contactApi.ts
│
├── pages/ # Top-level page components (React routes)
│ ├── HomePage.tsx
│ ├── HomePage.css
│ ├── MapPage.tsx
│ ├── MapPage.css
│ ├── InspirationPage.tsx
│ ├── InspirationPage.css
│ ├── CalendarPage.tsx
│ ├── CalendarPage.css
│ ├── ContactPage.tsx
│ └── ContactPage.css
│
├── routes/ # React Router setup
│ └── AppRoutes.tsx
│
├── styles/ # Global and layout-wide styles
│ ├── base.css # Reset, fonts, CSS variables
│ └── layout.css # App-wide grid/layout rules
│
├── hooks/ # Global custom React hooks
│ └── useWindowSize.ts
│
├── services/ # Shared utilities (e.g., API client)
│ └── httpClient.ts
│
├── types/ # Global TypeScript types and enums
│ └── common.ts
│
├── utils/ # Helper functions (date, formatting)
│ └── dateUtils.ts
│
├── App.tsx # Root component with layout and routing
├── App.css # App-level styles
└── main.tsx # React app entry point
