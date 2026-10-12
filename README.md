# MindVault 🧠

**Your thoughts. Your space. Your vault.**

MindVault is a clean, full-stack note-taking application built with the **MERN stack**. Create, view, edit, and delete notes through a responsive React interface backed by an Express API and MongoDB.

## Features

- Create notes with a title and content
- Browse saved notes in a responsive card layout
- Edit notes and delete them from the list or detail view
- Automatically sort notes by most recently updated
- Loading states and a helpful empty state
- Toast notifications for success and error feedback
- Client-side validation for required fields
- API rate-limiting support using Upstash packages
- Responsive dark interface built with Tailwind CSS

## Tech Stack

**Frontend:** React 19, Vite, React Router, Axios, Tailwind CSS 4, Lucide React, React Hot Toast

**Backend:** Node.js, Express 5, MongoDB, Mongoose, CORS, dotenv, Upstash Redis, Upstash Rate Limit

## Project Structure

```text
MindVault-MERN/
├── backend/
│   ├── src/
│   │   ├── config/       # Database connection
│   │   ├── controller/   # Note CRUD logic
│   │   ├── models/       # Mongoose schemas
│   │   └── routes/       # API routes
│   └── server.js
└── frontend/
    ├── public/
    └── src/
        ├── components/
        ├── lib/
        ├── pages/
        ├── App.jsx
        └── main.jsx
```

## Getting Started

### Prerequisites

- Node.js 18+
- npm
- MongoDB database (local or MongoDB Atlas)

### 1. Clone the repository

```bash
git clone https://github.com/saanisayyad/ThinkBoard-MERN.git
cd ThinkBoard-MERN
```

> The repository URL and folder name above remain unchanged until the GitHub repository itself is renamed.

### 2. Configure and run the backend

```bash
cd backend
npm install
```

Create a `.env` file in `backend/`:

```env
MONGO_URI=your_mongodb_connection_string
PORT=3000
```

Start the backend:

```bash
npm run dev
```

The API is available at `http://localhost:3000/api`.

### 3. Configure and run the frontend

In a second terminal:

```bash
cd frontend
npm install
npm run dev
```

The frontend defaults to `http://localhost:3000/api`. To use another API URL, create `frontend/.env`:

```env
VITE_API_URL=http://localhost:3000/api
```

### Production build

From the `frontend/` directory, run:

```bash
npm run build
npm run preview
```

## API Endpoints

All note endpoints use the `/api/note` route.

| Method | Endpoint | Description |
| --- | --- | --- |
| GET | `/api/note` | Retrieve all notes |
| GET | `/api/note/:id` | Retrieve a note |
| POST | `/api/note` | Create a note |
| PUT | `/api/note/:id` | Update a note |
| DELETE | `/api/note/:id` | Delete a note |

## Data Model

Each note includes a required `title`, required `content`, `createdAt`, and `updatedAt` timestamp.

## Security Notes

Keep database credentials and other secrets in environment variables. Never commit real credentials to the repository.

## Potential Improvements

Authentication, per-user notes, search and filtering, tags or categories, pagination, richer editing, and automated deployment.

---

Built with the MERN stack by **Mohammadsaani Sayyad**.
