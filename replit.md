# Tarcin Robotic LLP Official Website

## Overview

This is a full-stack web application for Tarcin Robotic LLP, a deep-tech startup based in Madurai, Tamil Nadu. The company specializes in robotics, IoT, AI, and educational technology solutions. The website serves as both a public-facing platform and includes a comprehensive Content Management System (CMS) for managing dynamic content.

## System Architecture

### Frontend Architecture
- **Framework**: React with TypeScript using Vite as the build tool
- **Routing**: Wouter for lightweight client-side routing
- **Styling**: Tailwind CSS with Shadcn/ui component library
- **State Management**: TanStack Query for server state management
- **Animations**: Framer Motion for component animations
- **UI Components**: Radix UI primitives with custom styling

### Backend Architecture
- **Framework**: Express.js with TypeScript
- **Database**: PostgreSQL with Drizzle ORM (schema defined but using JSON file storage currently)
- **Authentication**: JWT-based authentication for admin access
- **File Storage**: Local JSON files for content storage (blogs, events, careers, etc.)
- **Email Service**: Nodemailer integration for newsletter and contact forms

### Directory Structure
```
├── client/               # Frontend React application
│   ├── src/
│   │   ├── components/   # Reusable UI components
│   │   ├── pages/        # Page components
│   │   ├── hooks/        # Custom React hooks
│   │   ├── lib/          # Utilities and configurations
│   │   └── data/         # Static data files
├── server/               # Backend Express application
│   ├── cms/              # CMS-related routes and logic
│   └── routes.ts         # Main routing configuration
├── shared/               # Shared types and schemas
├── data/                 # JSON file storage for content
└── migrations/           # Database migration files
```

## Key Components

### Public Website Features
1. **Homepage**: Hero section, company narrative, features, stats, testimonials
2. **About**: Company mission, team information, timeline, values
3. **Services**: Educational solutions and implementation services
4. **Products**: Detailed product showcase with individual product pages
5. **Courses**: Training programs with detailed course information
6. **Blog**: Dynamic blog system with categorization and search
7. **Events**: Upcoming and past events management
8. **Careers**: Job postings with application system
9. **S2P Community**: Community stories and user engagement
10. **Contact**: Contact form with multiple inquiry types

### Admin CMS Features
1. **Authentication**: Secure login system for administrators
2. **Blog Management**: Create, edit, delete blog posts with rich content
3. **Event Management**: Manage upcoming and past events
4. **Career Management**: Post and manage job openings
5. **Community Management**: Moderate community stories and submissions
6. **Newsletter Management**: Handle email subscriptions
7. **Contact Management**: View and respond to contact inquiries

### UI/UX Features
- Responsive design optimized for mobile and desktop
- Internationalization support (English, Tamil, Arabic)
- Dark/light theme support
- Accessibility-compliant components
- Progressive loading and error handling
- SEO optimization with meta tags and structured data

## Data Flow

### Content Management Flow
1. Admin logs in through `/admin` route
2. JWT token stored in localStorage for subsequent requests
3. CRUD operations on content through protected API endpoints
4. JSON files updated in real-time
5. Public pages fetch updated content immediately

### User Interaction Flow
1. Public users browse content without authentication
2. Contact forms and newsletter subscriptions processed via API
3. File uploads handled for resume submissions
4. Community story submissions require moderation approval

## External Dependencies

### Frontend Dependencies
- **React Ecosystem**: React, React DOM, React Router (Wouter)
- **UI Components**: Radix UI primitives, Lucide React icons
- **Styling**: Tailwind CSS, Class Variance Authority
- **State Management**: TanStack Query
- **Forms**: React Hook Form with Zod validation
- **Animations**: Framer Motion
- **Utilities**: Date-fns, Axios, Chart.js

### Backend Dependencies
- **Server**: Express.js with TypeScript
- **Database**: Drizzle ORM with PostgreSQL driver (@neondatabase/serverless)
- **Authentication**: JSON Web Tokens
- **File Handling**: Multer for uploads
- **Email**: Nodemailer
- **Utilities**: UUID, Slugify, Dotenv

### Development Tools
- **Build Tools**: Vite, ESBuild
- **TypeScript**: Full TypeScript support with strict configuration
- **Code Quality**: ESLint, Prettier (implied by project structure)
- **Environment**: Cross-env for environment variable management

## Deployment Strategy

### Build Process
- Frontend builds to `dist/public` directory
- Backend compiles to `dist/index.js`
- Static assets served from public directory
- Environment variables managed through `.env` files

### Production Considerations
- Database migrations handled through Drizzle Kit
- JWT secrets must be configured in production environment
- Email service credentials required for contact/newsletter functionality
- File upload paths need proper permissions in production

### Scaling Considerations
- Current JSON file storage should migrate to PostgreSQL for production scale
- Image uploads should use cloud storage (AWS S3, Cloudinary)
- Email service should use professional SMTP provider
- Consider CDN for static asset delivery

## Changelog
- June 28, 2025. Initial setup

## User Preferences

Preferred communication style: Simple, everyday language.