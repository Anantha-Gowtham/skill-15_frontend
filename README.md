# Skill‑15 E‑commerce Frontend (React + Vite)

Modern React application built with Vite. This frontend consumes the Skill‑15 e‑commerce backend API.

## Prerequisites

- Node.js 18.18+ or 20+
- npm (bundled with Node.js)

## Getting started

### 1) Clone the repository

```
git clone https://github.com/Anantha-Gowtham/skill-15_frontend.git
cd skill-15_frontend
```

### 2) Install dependencies

```
npm install
```

### 3) Configure environment

Create a `.env` file in the project root to point the app to your backend API:

```
VITE_API_BASE_URL=http://localhost:8080
```

Adjust the URL for your environment or deployment domain.

### 4) Run in development

```
npm run dev
```

The app will start on a local development server (Vite default is `http://localhost:5173`).

## Available scripts

- `npm run dev` — start the development server
- `npm run build` — create a production build in `dist/`
- `npm run preview` — preview the production build locally
- `npm run lint` — run ESLint

## Project structure

- `src/`
	- `components/` — UI components
	- `services/` — API client and data access helpers
	- `context/` — React context providers/state
	- `assets/` — static assets
	- `App.jsx`, `main.jsx` — app entry points

## Connecting to the backend

- Ensure the backend service is running and reachable from the browser.
- For local development, configure `VITE_API_BASE_URL` to the backend base URL (for example, `http://localhost:8080`).
- If the backend enforces CORS, ensure the development origin (for example, `http://localhost:5173`) is allowed.

## Building for production

```
npm run build
```

The optimized static assets will be written to `dist/`. Serve `dist/` with any static web server. For example, an NGINX server block should route all SPA paths to `/index.html`.

## Troubleshooting

- "Network Error" or 4xx/5xx responses: verify `VITE_API_BASE_URL` and backend availability.
- Blank screen after build: ensure your server is configured to serve `index.html` for client‑side routes.
