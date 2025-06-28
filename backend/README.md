# Tarcin Robotic LLP - Backend API

This is the backend API server for Tarcin Robotic LLP website built with Express.js and TypeScript.

## Quick Start

1. Install dependencies:
```bash
npm install
```

2. Start the development server:
```bash
npm run dev
```

The API server will be available at: http://localhost:5000

## API Endpoints

### Public Endpoints
- `GET /api/cms/events` - Get events
- `GET /api/cms/events/upcoming` - Get upcoming events
- `GET /api/cms/events/past` - Get past events
- `GET /api/cms/careers` - Get career opportunities
- `GET /api/cms/careers/active` - Get active careers
- `GET /api/cms/community-stories` - Get approved community stories
- `POST /api/cms/community-stories/submit` - Submit new community story

### Admin Endpoints (Require Authentication)
- `POST /api/cms/auth/login` - Admin login
- `POST /api/cms/events` - Create new event
- `PUT /api/cms/events/:id` - Update event
- `DELETE /api/cms/events/:id` - Delete event
- `POST /api/cms/careers` - Create new career
- `PUT /api/cms/careers/:id` - Update career
- `DELETE /api/cms/careers/:id` - Delete career
- `PUT /api/cms/community-stories/:id/approve` - Approve community story
- `DELETE /api/cms/community-stories/:id` - Delete community story

## Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run start` - Start production server
- `npm run check` - Type check with TypeScript
- `npm run db:push` - Push database schema changes

## Technology Stack

- Express.js with TypeScript
- JWT authentication
- Drizzle ORM (with JSON file storage currently)
- Multer for file uploads
- Nodemailer for email services

## Data Storage

Currently using JSON files for data storage:
- `data/events.json` - Events data
- `data/careers.json` - Career opportunities
- `data/community-stories.json` - Community stories
- `data/blog-posts.json` - Blog posts
- `data/admin-users.json` - Admin users
- `data/subscribers.json` - Newsletter subscribers

## Authentication

Admin authentication uses JWT tokens. Default admin credentials can be found in `data/admin-users.json`.

## CORS Configuration

The server is configured to accept requests from `http://localhost:3000` for frontend development.