# Shopping Cart App

This repository contains a simple shopping cart application with a TypeScript backend (Express) and a React + Vite frontend.

## Repository structure

```
shopping-cart-app/
  backend/                # Express backend (TypeScript)
    src/
    tests/
    package.json
    tsconfig.json
  frontend/               # React + Vite frontend (TypeScript)
    src/
    package.json
    tsconfig.json
```

## Backend

The backend is an Express API written in TypeScript. It exposes endpoints under `/api`:

- `GET /api/products` - returns a list of products
- `POST /api/checkout` - accepts a checkout payload and returns order details
- `GET /health` - health-check endpoint

Quick start (local):

```powershell
cd shopping-cart-app/backend
npm ci
npm run dev        # runs ts-node-dev for development
# or to build and run compiled JS
npm run build
npm start
```

Notes:
- The server reads the port from `process.env.PORT` or defaults to `3001`.
- TypeScript build output goes to `dist/`.

Tests:

```powershell
cd shopping-cart-app/backend
npm test
```

## Frontend

The frontend is a React + Vite app written in TypeScript. API calls are made from `src/services/api.ts` where `API_BASE_URL` is currently set to `http://localhost:3001/api`.

Quick start (local):

```powershell
cd shopping-cart-app/frontend
npm ci
npm run dev
# Build for production
npm run build
# Preview production build
npm run preview
```

Deployment note:
- For production builds, prefer using an environment variable (Vite requires `VITE_` prefix) to configure the backend base URL. Example: set `VITE_API_BASE=https://your-backend.onrender.com/api` before building.

## Deployment (Render)

Backend (recommended config):
- Root Directory: `shopping-cart-app/backend`
- Build Command:
  - `npm ci && npm run build`
- Start Command:
  - `npm start` (which runs `node dist/server.js`)
- Health Check Path: `/health`
- Render provides `PORT` automatically; the server uses `process.env.PORT`.

Frontend (recommended config as a separate static site):
- Root Directory: `shopping-cart-app/frontend`
- Build Command:
  - `npm ci && npm run build`
- Publish Directory: value depends on Vite config (default is `dist`)
- Set the `VITE_API_BASE` env var in Render to point to the backend API URL before building.

## Vercel notes

If deploying the frontend to Vercel, make sure the project settings use `shopping-cart-app/frontend` as the root (or set the build command to `cd shopping-cart-app/frontend && npm ci && npm run build`).

If `tsc` fails during Vercel build, the options are:
- Fix TypeScript errors shown by `tsc`.
- Or change frontend `package.json` build script to `vite build` to skip `tsc` in CI (faster but skips type checking on CI).

## Environment variables

Do not commit secrets to the repo. Example environment variables you may want to set in deploy targets:

- `VITE_API_BASE` - frontend build-time API base URL, e.g. `https://api.example.com/api`
- `NODE_ENV=production` - backend
- Any DB_URL, SECRET keys, etc. — add them in the hosting provider's dashboard.

## Cleanup (recommended)

- Add `dist/` to `.gitignore` and avoid committing compiled artifacts.
- Keep only `src/*.ts` in the backend; remove any redundant `src/server.js` copies to avoid confusion.

## Contact

If you want, I can:
- Add `.env.example` and optional dotenv in development.
- Add a `render.yaml` for one-click Render deployment.
- Fix any TypeScript build errors reported by `tsc` (paste the errors and I’ll fix them).

Happy to help further — tell me which next step you want.