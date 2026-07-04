# react-node-test-assessment

## Repository Layout
- `api/` – Express backend (messages, file uploads)
- `app/` – React frontend scaffold

## Prerequisites
- Node.js 22+
- pnpm (recommended) or npm

## Quick Start
```bash
# backend
cd api
cp env.example .env     # set Pusher credentials (optional)
pnpm install
pnpm dev                # starts on http://localhost:3001

# frontend
cd ../app
cp env.example .env     # set Pusher credentials (optional)
pnpm install
pnpm dev                # starts on http://localhost:3000
```

**Note:** No database setup required! The app uses in-memory storage for messages. Messages will be lost on server restart, but file uploads persist.

## Completed Challenges

1) **Real-time messages with Pusher (backend + frontend)**  
   - Wired up Pusher on the backend to publish `new-message` and `message-deleted` events when messages are created/deleted.  
   - On the frontend, initialized Pusher and subscribed to the same channel/events to live-update the message list.
   - Added `.env` entries for Pusher keys (backend + frontend).
   - **How to run with Pusher:**
     1. Copy `api/env.example` to `api/.env` and fill in `PUSHER_APP_ID`, `PUSHER_KEY`, `PUSHER_SECRET`, and `PUSHER_CLUSTER`.
     2. Copy `app/env.example` to `app/.env` and fill in `REACT_APP_PUSHER_KEY` and `REACT_APP_PUSHER_CLUSTER`.

2) **Message search endpoint + realtime filter (backend + frontend)**  
   - Added `GET /api/messages/search?q=term` (case-insensitive, newest first, non-empty `q`, max 100 results).  
   - Added a search input in the UI that hits this endpoint with a 300ms debounce and shows loading/empty states.  
   - When not searching, the live Pusher-powered feed is shown. When searching, filtered results are displayed without breaking realtime updates once the search is cleared.

## Important Notes:
- **No AI Tools**: This assessment was completed manually without the use of AI tools like ChatGPT or Copilot.
