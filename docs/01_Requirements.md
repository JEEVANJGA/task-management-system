# 📌 Project Requirements – Task Management System (TMS)

## 🎯 Objective

Develop a **scalable Task Management System** as a single‑page application (SPA) that lets users create, manage, and track tasks. Initially, the solution will be **frontend‑only** (using mock data or localStorage). After completing the frontend, a backend (REST/GraphQL API) will be integrated.

## 🚀 Key Features

- **User Authentication:** Google OAuth login/signup (simulated initially).
- **Task Management:** CRUD operations for tasks.
- **Task Assignment:** Assign tasks to users.
- **Task Filters & Sorting:** Search, filter by status and priority, and sort tasks.
- **File Upload:** Attach files to tasks.
- **Real-Time Updates:** Use WebSockets for instant changes (future phase).
- **Dashboard & Analytics:** Visual representation and summaries of tasks.
- **User Management:** Manage users and teams.
- **Responsive UI:** Implement using Ant Design and Tailwind CSS.
- **Testing & Deployment:** Automated tests (TDD) and deployment via GitHub Pages.

## 🎯 Core Features

1. **User Authentication**
   - Login & Logout (mocked initially; real authentication later)
2. **Task Management**
   - Create, Edit, Delete, and View tasks
   - Set Priority and Due Dates
3. **Task Status Tracking**
   - Kanban-style drag-and-drop board
   - Filter tasks by status and priority
4. **User Notifications (Future)**
   - Reminders for due tasks
5. **Analytics & Reporting (Future)**
   - Task completion trends

## 📌 Non-Functional Requirements

- **Scalability:** Modular, component‑based architecture.
- **Performance:** Optimized rendering with React’s latest features.
- **Testing:** TDD-driven development with high test coverage.

## 🚀 Development Phases

### Phase 1: Frontend-Only
- Use mock data (or localStorage) for tasks and user data.
- Build full UI components with state management, routing, and interactions.
- Implement all core features.
- Ensure the app is responsive and well‑styled.
- Use the latest React (v19.0.0) and React Router DOM (v7.1.5).

### Phase 2: Backend Integration
- Replace mock data with API calls.
- Integrate real authentication, persistent storage, and real‑time updates.
- Migrate state and data management from mock/local to remote APIs.

## 📂 Initial Project Folder Structure

Below is a proposed folder structure for the frontend project. This structure is a starting point and can be modified as needed throughout development:

```
/tms
├── /public
│   └── index.html         # Main HTML file
├── /src
│   ├── /assets            # Images, icons, and styles
│   ├── /components        # Reusable UI components (e.g., TaskForm, TaskList)
│   ├── /context           # Global state management (e.g., AuthContext)
│   ├── /hooks             # Custom React hooks
│   ├── /pages             # Application pages (e.g., Dashboard, Login)
│   ├── /routes            # Routing configuration using React Router DOM
│   ├── /services          # API calls and business logic (mock or real)
│   ├── /tests             # Unit and integration tests (TDD)
│   ├── /utils             # Helper functions and utilities
│   ├── App.tsx            # Root component
│   └── index.tsx          # Application entry point
├── /docs                  # Documentation (Requirements, Screens, Features, etc.)
│   ├── 01_Requirements.md
│   ├── 02_Screens.md
│   ├── 03_Features.md
│   ├── 04_Technical_Stack.md
│   ├── 05_Development_Plan.md
│   ├── 06_Testing_Strategy.md
│   ├── 07_Deployment.md
│   └── 08_TDD_Approach.md
├── .eslintrc.config.js    # ESLint configuration
├── package.json           # Project dependencies and scripts
└── README.md              # Project overview and instructions
```


## 📝 Note

- The initial phase will use **mock data** and/or **localStorage** to simulate persistence.
- Future updates (Phase 2) will integrate a backend API and real‑time features.
- The Project folder structure is a suggested starting point; feel free to adjust it as your project grows.


