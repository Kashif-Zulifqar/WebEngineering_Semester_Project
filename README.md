Collecting workspace information```markdown

# DisneyClone — Netflix-style UI (React + Vite)

A responsive Netflix-style frontend with a minimal Express backend for movie lookups (TMDB) and simple user auth examples. Built as a portfolio project showcasing React, Vite, Firebase auth helpers and a lightweight Node/Mongo backend.

---

## Features

- Responsive UI with hero banner, horizontal title carousels and hover effects.
- Movie search and trailer play via TMDB (video fetch in backend).
- Authentication scaffolding (client-side context + Firebase helpers).
- Simple Express backend with user controllers and movie-video lookup.
- Clean component structure for quick iteration and portfolio demos.

Key components and endpoints:

- Frontend entry: [`App`](src/App.jsx) — [src/App.jsx](src/App.jsx)
- Auth provider: [`StateManager`](src/AuthContext.jsx) — [src/AuthContext.jsx](src/AuthContext.jsx)
- Pages: [`Login`](src/Pages/Login/Login.jsx) — [src/Pages/Login/Login.jsx], [`Home`](src/Pages/Home/Home.jsx) — [src/Pages/Home/Home.jsx], [`Player`](src/Pages/Player/Player.jsx) — [src/Pages/Player/Player.jsx]
- Firebase helpers: [`signup`, `login`, `logout` exports](`src/Firebase.js`) — [src/Firebase.js](src/Firebase.js)
- Backend entry: [Backend/entry.mjs](Backend/entry.mjs) — movie video fetch: [`getMovies`](Backend/Controller/Movies.Controller.mjs) — [Backend/Controller/Movies.Controller.mjs](Backend/Controller/Movies.Controller.mjs)
- Footer author: [src/Components/Footer/Footer.jsx](src/Components/Footer/Footer.jsx)

---

## Tech Stack

- Frontend: React 18 + Vite ([vite.config.js](vite.config.js))
- Styling: CSS modules / plain CSS (component CSS files in src)
- HTTP: axios
- Auth helper: Firebase (client) — [src/Firebase.js](src/Firebase.js)
- Backend: Node + Express, Mongoose (MongoDB) — backend in [Backend/](Backend)
- API: TMDB (used in backend controller)

---

## Quick Install (local)

Requirements: Node.js (14+), npm

1. Clone repository

   ```sh
   git clone <repo-url>
   cd DisneyClone
   ```

2. Install frontend deps

   ```sh
   npm install
   ```

3. Install backend deps and start backend

   ```sh
   cd Backend
   npm install
   npm start
   ```

   Backend entry: entry.mjs

4. Start frontend (from repo root)
   ```sh
   cd ..
   npm run dev
   ```
   Frontend entry: main.jsx

Notes:

- API endpoints served on port 1000 by default (see Backend/entry.mjs).
- MongoDB connection string is set in database.mjs. Replace with environment variables for production.

---

## Common scripts

Frontend (root) — see package.json

- npm run dev — start Vite dev server
- npm run build — build production bundle
- npm run preview — preview production build
- npm run lint — run ESLint

Backend — see package.json

- npm start — nodemon entry.mjs (dev server)

---

## Folder structure (concise)

- index.html
- package.json
- vite.config.js
- Backend/
  - entry.mjs
  - database.mjs
  - Controller/
    - Movies.Controller.mjs
    - User.Controller.mjs
  - Models/
    - Movies.mjs
    - Client.mjs
- src/
  - main.jsx
  - App.jsx
  - AuthContext.jsx
  - Firebase.js
  - Components/
    - Navbar, Footer, TitleCards (see component files)
  - Pages/
    - Login/Login.jsx
    - Home/Home.jsx
    - Player/Player.jsx

---

## Usage examples

- Open the app: http://localhost:5173 (Vite default) after `npm run dev`.
- Login page at `/` — see Login.jsx.
- After login, visit `/home` — title carousels are rendered by `Titlecards` which link to `/Player/:id`.
- Player page `/Player/:id` loads movie trailers using backend route GET /movies/:id (see MoviesRoutes.mjs → getMovies).

Example: click a card on Home (cards fetch TMDB lists) → opens `/Player/12345` and plays trailer.

---

## Contributing

1. Fork the repo and create a feature branch.
2. Keep commits focused and use clear messages.
3. Open a PR describing changes and include screenshots if UI-related.
4. For backend changes, prefer environment variables for secrets (do not commit keys).

Recommended files to update for large changes:

- Frontend routes: App.jsx
- Auth flow: AuthContext.jsx
- Backend API controllers: Backend/Controller/\*.mjs

---

## License

MIT — see LICENSE (apply MIT in your portfolio repos).

---

## Contact

Kashif Zulifqar — shown in app footer: Footer.jsx

---

Small, polished demo ideal for portfolio pages and further extension (improved auth flows, env-based configs, additional TMDB features).
