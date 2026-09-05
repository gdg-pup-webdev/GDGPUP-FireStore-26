# Express StudyJam: Routes, Views & Todo App

[![Status: Teaching](https://img.shields.io/badge/Status-Teaching-blue)](docs/state.md)
[![Stack: Firebase](https://img.shields.io/badge/Stack-Firebase-black)](#about)
[![FMD philosophy: 1.31.0](https://img.shields.io/badge/FMD%20philosophy-1.31.0-blue)](AGENTS.md)


This repository contains the materials used in a StudyJam that demonstrates how a small Express backend can serve a vanilla JavaScript front-end. The project is a compact Todo application used to teach routing, CRUD operations, and DOM-driven UI updates.

## Table of Contents

- [About](#about)
- [Start here](#start-here)
- [Repository Structure](#repository-structure)
- [Technologies](#technologies)
- [Quick start](#quick-start)
- [API Endpoints](#api-endpoints-demo)
- [Learning Outcomes](#learning-outcomes)
- [Activities & Challenges](#activities--challenges)
- [Contributing](#contributing)
- [Documentation](#documentation)
- [Contributors](#contributors)

## About

Hands-on StudyJam materials for GDG PUP: a minimal Express server plus vanilla JS Todo UI. Aimed at learners who want routing, CRUD, and `fetch`-driven DOM updates without a frontend framework.

## Start here

- **Humans:** this README, then [docs/state.md](docs/state.md)
- **Agents:** [AGENTS.md](AGENTS.md) (state → index → FLAGS)
- **Contributors:** table below

## Repository Structure

Explore the key files and folders below.

|                  |                                                                                                     |
| ---------------- | --------------------------------------------------------------------------------------------------- |
| **Use this if:** | You want a minimal, hands-on example of Express routes connected to a front-end without frameworks. |
| **Contains:**    | Server entry, route handlers, and the `views` folder that holds the client app.                     |

### Important paths

- `app.js` - server bootstrap and middleware registration.
- `routes/route.js` - CRUD routes for the Todo API and the root route serving the app.
- `views/` - frontend: `index.html`, `index.css`, `index.js` (UI, layout, client logic).
- `render.js` - helper to resolve view files for responses.
- `todo.json` - file-based storage used for demo persistence.

## Technologies

| Technology        | Purpose                                 |
| ----------------- | --------------------------------------- |
| Node.js + Express | Server and route handling               |
| HTML / CSS        | Frontend markup and styling             |
| JavaScript (ES6)  | Frontend logic, state and `fetch` calls |

## Quick start

1. Clone or download this repository.
2. Install dependencies (if present) and start the server:

```bash
npm install
node app.js
# or use the project's start script when available:
npm start
```

3. Open `http://localhost:3000` (or the port logged by the server).

Tips: edit `views/index.js` to experiment with client behaviour; update `routes/route.js` to practice server-side logic.

## API Endpoints (Demo)

- `GET /todos` - list all todos
- `POST /todos` - create `{ task: string }`
- `GET /todos/:id` - get a single todo
- `PATCH /todos/:id` - update `{ task?, done? }`
- `DELETE /todos/:id` - remove a todo

Use `curl`, Postman, or the app UI to interact with these endpoints.

## Learning Outcomes

- Map Express routes to frontend actions using `fetch`.
- Implement and test CRUD behavior in a tiny app.
- Practice DOM manipulation and lightweight state handling without libraries.

## Activities & Challenges

| Activity          | Description                                                                           |
| ----------------- | ------------------------------------------------------------------------------------- |
| **Main app**      | Inspect `views/index.html` + `views/index.js` to see how the UI uses the API.         |
| **Hands-on**      | Replace `todo.json` with a small DB (lowdb/SQLite) and persist todos across restarts. |
| **Accessibility** | Improve keyboard navigation and ARIA roles in the UI.                                 |

Suggested exercises:

- Add a `/stats` route that returns counts (active/total/done).
- Add per-user todo lists (no auth required - simulate users by query param).

## Contributing

Contributions and improvements are welcome. Please open a focused PR and document any new scripts or commands in this README.

## Documentation

| Doc | Purpose |
|-----|---------|
| [State](docs/state.md) | Teaching position / handover |
| [Index](docs/index.md) | Doc inventory |
| [FLAGS](FLAGS.md) | Improvement register |
| [AGENTS](AGENTS.md) | Agent load order |

## Contributors

This project is made possible by the GDG PUP community.

| Name | Role | GitHub |
| --- | --- | --- |
| [Carlos Jerico Dela Torre](https://www.linkedin.com/in/delatorrecj) | Chief Technology Officer (2025-2026) | [@delatorrecj](https://github.com/delatorrecj) |
| [Keith Justine A. Virgenes](https://www.linkedin.com/in/keith-justine-virgenes-749225302) | Backend Developer / QA | [@jhonkeithman123](https://github.com/jhonkeithman123) |

