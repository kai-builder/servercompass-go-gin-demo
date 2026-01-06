# Server Compass Go Gin Demo

A minimal Gin application that surfaces public environment variables with safe defaults while keeping private values on the server.

## Features
- Shows public environment variables with fallback to `Not set` when missing
- JSON endpoint at `/api/env` returning the same public values
- Private environment variables stay server-side and are not exposed to the browser

## Getting Started
1. Install Go (1.21+ recommended).
2. Copy `.env.example` to `.env` (optional) and adjust values:
   ```bash
   cp .env.example .env
   ```
3. Start the server:
   ```bash
   go run main.go
   ```
4. Visit `http://localhost:8080` for the UI or `http://localhost:8080/api/env` for JSON.

## Environment Variables
Public (shown in UI/API):
- `APP_NAME`
- `API_URL`
- `ENVIRONMENT`
- `VERSION`

Private (server-only):
- `DATABASE_URL`
- `API_SECRET_KEY`

Unset variables render as `Not set` so you can see what is missing during development.
