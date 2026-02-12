# Talent IQ - Interview Platform

A full-stack application for conducting technical interviews with real-time code execution, video communication, and instant feedback.

## Features

- VSCode-powered code editor with syntax highlighting
- Secure authentication with Clerk
- 1-on-1 video interview rooms with screen sharing
- Real-time chat messaging between participants
- Live code execution with test case validation
- Dashboard with session statistics
- Practice problems for solo coding practice
- Room access control (2 participants max)
- Background job processing for async operations
- REST API built with Node.js and Express
- Data caching and optimization with TanStack Query

## Tech Stack

**Backend:**

- Node.js & Express
- MongoDB for data persistence
- Clerk for authentication
- Stream.io for video and chat
- Inngest for background jobs

**Frontend:**

- React with Vite
- TanStack Query for data fetching
- Stream.io React SDK

## Environment Variables

### Backend Setup

Create a `.env` file in the `backend/` directory with the following variables:

```
PORT=3000
NODE_ENV=development

DB_URL=your_mongodb_connection_url

INNGEST_EVENT_KEY=your_inngest_event_key
INNGEST_SIGNING_KEY=your_inngest_signing_key

STREAM_API_KEY=your_stream_api_key
STREAM_API_SECRET=your_stream_api_secret

CLERK_PUBLISHABLE_KEY=your_clerk_publishable_key
CLERK_SECRET_KEY=your_clerk_secret_key

CLIENT_URL=http://localhost:5173
```

### Frontend Setup

Create a `.env.local` file in the `frontend/` directory:

```
VITE_CLERK_PUBLISHABLE_KEY=your_clerk_publishable_key
VITE_API_URL=http://localhost:3000/api
VITE_STREAM_API_KEY=your_stream_api_key
```

## Installation & Running

### Backend

```bash
cd backend
npm install
npm run dev
```

The backend will run on `http://localhost:3000`.

### Frontend

```bash
cd frontend
npm install
npm run dev
```

The frontend will run on `http://localhost:5173`.
