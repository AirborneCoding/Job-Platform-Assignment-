# Job Platform Assignment

A full-stack job platform web application built as a take-home assignment.  
It allows users to view job positions, see details, and apply with their resume.  
Includes a minimal admin area for managing positions and viewing applications.

---

## 🧠 Project Architecture

The project has **three main folders** inside the repository:

1. **server** — Express + TypeScript backend with PostgreSQL + DrizzleORM.
2. **upload_resumes** — Folder where resumes are stored.
3. **client** — React + TypeScript frontend with TanStack.

---

## Backend (server)

### Setup & Running

```bash
cd server
npm install
````

1. Create a `.env` file in the `server` folder:

```env
PORT=5000
DATABASE_URL="add_postgres_database_url"
```

2. Ensure your PostgreSQL database exists.
3. Run the server:

```bash
npm run dev
```

> Running the server will automatically seed job positions in the database.
> Server runs at `http://localhost:5000`.

### Structure & Features

* Standard Express setup: `app.ts`, middleware, error handling.
* **Database folder (`db`)**: connection, migrations, seed data.

  * **Seed data:** Positions are automatically seeded.
* **Controllers, routes, schemas** (note: schemas are combined in one file) are organized by feature.
* Environment variables are required for local setup.

---

## Upload Resumes

* The `upload_resumes` folder stores resumes (PDFs).
* Ensure this folder exists and is writable before running the server.

---

## Frontend (client)

### Setup & Running

```bash
cd client
npm install
npm run dev
```

> Ensure the backend is running before starting the frontend.
> Frontend runs at `http://localhost:5173`.

### Structure & Features

* React app with TypeScript, TanStack, and API functions connecting to the backend.
* **Pages:**

  * `Home` — Landing page
  * `Positions` — Job listings
  * `PositionDetail` — Job detail view
  * `Admin` — Admin area for managing positions and viewing applications
* **Components & common folders:** `assets`, `utils`, `custom` for UI and helper functions.

---

## 📝 Notes & Key Decisions

* **Backend:** TypeScript + Express + DrizzleORM for structure and type safety.
* **Frontend:** React + TanStack for modern state management and UI.
* **Seed Data:** Positions are seeded automatically when running the server.
* **Environment:** `.env` file required for DB URL and server port.
* Focus was on completing core functionality within the deadline; some parts may not be perfect.

---

## 🏁 Usage

* Access frontend: `http://localhost:5173`.
* Admin area: `/admin` (manage positions, view applications).
* API endpoints: `http://localhost:5000`.

``
## This version:  
- Focus was on completing core functionality within the deadline; some parts may not be perfect.
- Starts with **backend first**, then **uploads**, then **frontend**.  
- Clear **setup instructions**, commands, and ports.  
- Simple **architecture & key decisions** section.  
- Looks professional but still like something you would write yourself.  