# Tarcin Robotic LLP - Localhost Development Setup

This project has been restructured for localhost development with separate frontend and backend folders.

## Project Structure

```
├── frontend/          # React frontend application (Port 3000)
├── backend/           # Express.js API server (Port 5000)
├── client/            # Original integrated client files
├── server/            # Original integrated server files
└── data/              # Shared data files
```

## Quick Start Guide

### 1. Backend Setup (API Server)

```bash
cd backend
npm install
npm run dev
```

The backend API will run on: **http://localhost:5000**

### 2. Frontend Setup (React App)

```bash
cd frontend
npm install
npm run dev
```

The frontend will run on: **http://localhost:3000**

## Communication Flow

- Frontend (localhost:3000) ↔ Backend (localhost:5000)
- Frontend automatically proxies API calls to the backend
- CORS is configured on the backend to allow frontend requests
- All API endpoints are available at `http://localhost:5000/api/...`

## Key Features

### Frontend (Port 3000)
- React 18 with TypeScript
- Vite development server
- Tailwind CSS styling
- Component library with Shadcn/ui
- Real-time API communication with backend

### Backend (Port 5000)
- Express.js API server
- JWT authentication
- JSON file-based data storage
- CORS enabled for frontend communication
- Complete CMS functionality

## Development Workflow

1. Start the backend server first: `cd backend && npm run dev`
2. Start the frontend server: `cd frontend && npm run dev`
3. Access the application at http://localhost:3000
4. API calls will automatically route to http://localhost:5000

## Original Integrated Setup

The original integrated setup files are preserved in:
- `client/` - Original frontend files
- `server/` - Original backend files

These can still be used for Replit deployment or integrated development.

## Admin Access

Default admin credentials can be found in `backend/data/admin-users.json`
Access the admin panel at: http://localhost:3000/admin