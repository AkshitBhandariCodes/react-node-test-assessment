<<<<<<< HEAD
# Test Project

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

## Simple Challenges

1) **Real-time messages with Pusher (backend + frontend)**  
   - Wire up Pusher on the backend to publish `new-message` and `message-deleted` events when messages are created/deleted.  
   - On the frontend, initialize Pusher and subscribe to the same channel/events to live-update the message list (append on new-message, remove on message-deleted).  
   - Add `.env` entries for Pusher keys (backend + frontend) and document how to run with them.

2) **Message search endpoint + realtime filter (backend + frontend)**  
   - Add `GET /api/messages/search?q=term` (case-insensitive, newest first, non-empty `q`, max 100 results).  
   - Add a search input in the UI that hits this endpoint with a 300ms debounce and shows loading/empty states.  
   - When not searching, keep showing the live Pusher-powered feed from Challenge 1; when searching, show filtered results without breaking realtime updates once the search is cleared.

## Submission Guidelines

After completing your challenges:

1. **Update README**: Document which challenges you completed and any additional setup required
2. **Submit Your Work**:
   - Add this repository to your GitHub account
   - Send an email back with the repository link
   - We will review your submission and get back to you

**Important Notes:**
- **No AI Tools**: Please do not use AI tools like ChatGPT or Copilot for this assessment. We want to evaluate your own coding abilities and problem-solving skills.
=======
# react-node-test-assessment
>>>>>>> 94225b19fc2863d1403687fb12d940baa48775ce
