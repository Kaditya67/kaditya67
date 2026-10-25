# Personal Projects Deep-Dive: Architecture, Implementation & Resume Metrics

This document provides a thorough analysis of your **4 Personal Projects**:
1. **[WebManager](file:///d:/Alive/Practice/github/WebManager)** (MERN Stack: React, Express, MongoDB, Node.js)
2. **[PlannerX](file:///d:/Alive/Practice/github/PlannerX)** (MERN Stack: React, Express, MongoDB, Node.js)
3. **[knowledge-map](file:///d:/Alive/Practice/github/knowledge-map)** (MERN Stack: React, Express, MongoDB, Node.js)
4. **[goal-tracker](file:///d:/Alive/Practice/github/goal-tracker)** (Python / Django 5.1 & YouTube Data API v3)

---

## 🌐 1. [WebManager](file:///d:/Alive/Practice/github/WebManager) (MERN Stack Platform)
> **Domain**: DevOps / Cloud Infrastructure & Microservice Topology Management  
> **Architecture**: Decoupled Monorepo (`/client` Vite React + `/server` Node.js Express REST API)

### 🛠️ Exact Tech Stack
- **Frontend**: React 19, Vite, Tailwind CSS, Custom High-Density Developer UI System.
- **Backend**: Node.js, Express.js (`server/`), Morgan logger, Cookie-parser, Dotenv.
- **Database / ODM**: MongoDB via Mongoose ODM.
- **Security**: JWT (`jsonwebtoken`) cookie-based authentication, Bcrypt password encryption.

### 🧠 Engineering Capabilities You Built
1. **Multi-Tier Microservice Topology**:
   - Built a hierarchical schema modeling software systems into decoupled tiers: `frontend`, `backend`, `database`, `worker`, `mobile`, and `other`.
   - Tracks environment ports, git branch linkages, and operational statuses (`healthy`, `degraded`, `offline`).
2. **Global Deployments Matrix**:
   - Engineered a searchable matrix indexing live application deployments across `production`, `staging`, `development`, and `preview` environments.
   - Provides 1-click URL copying, deployment health badges, and instant environment switching.
3. **Bidirectional Cloud Host Mapping**:
   - Built a cloud infrastructure registry mapping third-party providers (AWS, Vercel, Supabase, Cloudflare, Railway) directly to the application components hosted on them.
4. **DevEx-Focused UI (Linear / Vercel Aesthetic)**:
   - Compact, information-dense layout utilizing Inter and JetBrains Mono typography, dark/light theme switching, and mobile bottom-sheet drawers.

### 📝 Resume Bullet Points
- *Architected a full-stack MERN developer platform to map, visualize, and monitor microservice topologies, multi-tier components, and cloud infrastructure providers.*
- *Designed a real-time deployments matrix tracking live application endpoints across staging and production environments with a high-density Linear/Vercel-inspired UI.*
- *Implemented secure JWT authentication and role-based access with MongoDB Mongoose schemas modeling bidirectional relationships between cloud hosts and microservices.*

---

## ⚡ 2. [PlannerX](file:///d:/Alive/Practice/github/PlannerX) (MERN Stack SaaS)
> **Domain**: Productivity Engineering & Scenario-Driven Roadmap Execution  
> **Architecture**: Decoupled Monorepo (`/frontend` React + `/backend` Express REST API)

### 🛠️ Exact Tech Stack
- **Frontend**: React, Vite, Tailwind CSS v4 (`@tailwindcss/vite`), Date-fns, Lucide Icons, Axios.
- **Backend**: Node.js, Express.js, Express-Rate-Limit (DDoS protection), Helmet (HTTP security headers), Validator.
- **Database / ODM**: MongoDB with Mongoose ODM (`backend/config/db.js`).
- **Security**: JWT authorization, Bcrypt.js, Express-async-handler, cookie-based session tokens.

### 🧠 Engineering Capabilities You Built
1. **Hierarchical Task Tree State Engine**:
   - Engineered a nested planning architecture dividing plans into collapsible sections and atomic sub-tasks with real-time percentage completion rollups.
   - Designed lifecycle status filters: `Active`, `Stashed` (on-hold), and `Archived` (historical records with 1-click restore).
2. **Pristine JSON Template Import/Export Engine**:
   - Built an algorithm that serializes complete complex roadmaps into portable JSON schema files.
   - Features automated state sanitation: strips session logs and resets all completion checkboxes to 0% so roadmaps can be shared as clean templates.
3. **Workspace Domain Isolation**:
   - Provides segregated workspaces (Engineering, Design, Operations, Personal) ensuring zero cross-context data leaks.
4. **Deep Focus Session Engine**:
   - Built-in Pomodoro, Deep Work, and Custom interval timers linked directly to active roadmap items with LocalStorage session recovery.

### 📝 Resume Bullet Points
- *Built a full-stack MERN productivity SaaS featuring hierarchical task-tree state engines, workspace isolation, and real-time completion analytics.*
- *Engineered a JSON template engine enabling 1-click export and import of reusable project roadmaps with automatic state sanitation and resetting.*
- *Hardened the backend API using Helmet, Express-Rate-Limit, and JWT cookie authentication with modular Mongoose schemas.*

---

## 🗺️ 3. [knowledge-map](file:///d:/Alive/Practice/github/knowledge-map) (MERN Stack Knowledge Hub)
> **Domain**: Personal Knowledge Base & Resource Tagging Engine  
> **Architecture**: Decoupled Monorepo (`/frontend` React + `/backend` Express REST API)

### 🛠️ Exact Tech Stack
- **Frontend**: React, React Router DOM, Tailwind CSS, Lucide Icons, Axios, React-Markdown, Remark-GFM.
- **Backend**: Node.js, Express.js (`server.js`), Cors, Dotenv.
- **Database / ODM**: MongoDB via Mongoose ODM (`models/Asset.js`).
- **Tooling**: Postman collection test suite (`backend/postman/Knowledge-Hub-API.postman_collection.json`).

### 🧠 Engineering Capabilities You Built
1. **Multi-Type Asset Tagging & Categorization**:
   - Flexible MongoDB schema (`Asset.js`) capable of indexing documentation, articles, reading lists, and tech guides with custom tags.
2. **Markdown Rendering with GFM**:
   - Client-side rendering pipeline utilizing `react-markdown` and `remark-gfm` for formatted code blocks, tables, and notes.
3. **Structured API Verification**:
   - Full Postman collection test suite covering authentication, CRUD endpoints, and search parameters.

### 📝 Resume Bullet Points
- *Developed a MERN stack personal knowledge management application with dynamic categorization, tagging, and Markdown GFM rendering.*
- *Designed RESTful API endpoints in Express with MongoDB Mongoose schemas, validated via an automated Postman test suite.*

---

## 🎯 4. [goal-tracker](file:///d:/Alive/Practice/github/goal-tracker) (Django & External API Integration)
> **Domain**: Learning Milestones & Media Progress Tracking  
> **Architecture**: Django 5.1 Project (`goal_tracker/tracker/`)

### 🛠️ Exact Tech Stack
- **Backend**: Python 3.10+, Django 5.1, Django ORM, SQLite/PostgreSQL.
- **Third-Party API**: YouTube Data API v3 (via Python `requests`).
- **Configuration**: `python-decouple` for environment variables.
- **Frontend**: Django Templates, CSS3, JavaScript.

### 🧠 Engineering Capabilities You Built
1. **YouTube Data API v3 Ingestion**:
   - Ingests public YouTube playlists via URL, extracting playlist IDs, querying Google's API, and parsing video snippets, duration, and high-res thumbnails.
2. **Milestone Watch Tracking**:
   - Allows users to mark individual videos as watched/unwatched, computing real-time course progress percentages.
3. **Centralized Visual Dashboard**:
   - Clean Django views and templates rendering total playlists, completed counts, and pending study hours.

### 📝 Resume Bullet Points
- *Engineered a learning milestone tracking application in Django 5.1 integrating the YouTube Data API v3 to automate playlist metadata ingestion.*
- *Implemented real-time course progress tracking, completion analytics, and user session management with the Django ORM.*
