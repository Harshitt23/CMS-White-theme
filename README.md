# Dabas EV CMS (Admin Portal)

This repository contains the **Dabas EV CMS / Admin Portal**, delivered as a **freelance engagement** for **Dabas EV Company** to support day-to-day operational management of EV charging infrastructure and business workflows from a centralized dashboard.

## What we delivered

- **Admin dashboard** for operational visibility
- **Charger & station management** (stations, chargers, profiles, logs, and map view)
- **Company & client management** screens
- **Billing & payments** area (charging sessions + licensing)
- **User management** (including administrator section)
- **Notifications** and **complaints** screens
- **Theme system** (light/dark) and a reusable UI component set

## Tech stack

- **Next.js (App Router)** + **React** + **TypeScript**
- **Tailwind CSS** (with utility merging) + **MUI** + **Radix UI**
- **Zustand** for state management
- **AG Grid / AG Charts** + **Chart.js** for analytics/visualization
- **Leaflet / React-Leaflet** for map views

## Local setup

### Prerequisites

- **Node.js**: 18+ recommended (20+ preferred)
- **npm** (or your preferred package manager)

### Install

```bash
npm install
```

### Environment variables

Create a `.env.local` in the project root:

```bash
# Backend base endpoint for stations/chargers listing
NEXT_PUBLIC_BE_URL=

# Heartbeat endpoint (expects `?stationId=...`)
NEXT_PUBLIC_HEARTBEAT_URL=

# Charger profile API base (the app calls `${NEXT_PUBLIC_PROFILE_API}/${profileId}`)
NEXT_PUBLIC_PROFILE_API=
```

If these are not set or the backend is unreachable, the UI will fall back to **dummy data** for a smoother local/demo experience.

### Run (development)

```bash
npm run dev
```

Open `http://localhost:3000`.

## Useful scripts

- **`npm run dev`**: start local dev server
- **`npm run build`**: production build
- **`npm run start`**: run the production server
- **`npm run lint`**: run ESLint

## Deployment notes

This is a standard Next.js application and can be deployed on:

- **Vercel** (recommended for simplest deployment), or
- Any Node.js hosting that supports `next build` + `next start`

Make sure the same environment variables from `.env.local` are configured in the hosting provider.

## Project structure (high level)

- **`app/`**: routes, layouts, and UI for modules (dashboard, charger, company, bills, users, etc.)
- **`hooks/`**: data-fetching hooks (with graceful fallbacks)
- **`components/`** + **`app/components/`**: reusable UI components and module components
- **`store/`**: global state (Zustand)
- **`lib/`**: utilities, types, and shared helpers

## Client / ownership

This project was implemented for **Dabas EV Company**. Source code and branding are intended for internal business use unless otherwise agreed.

sdsa