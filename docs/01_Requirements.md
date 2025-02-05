# 📌 Project Requirements – Task Management System (TMS)

## 🎯 Objective

Develop a **scalable Task Management System** as a single-page application (SPA) that lets users create, manage, and track tasks. Initially, the solution will be **frontend-only** (using mock data or local storage). After completing the frontend, a backend (REST/GraphQL API) will be integrated.

## 🚀 Key Features

- **User Authentication**: Google OAuth login/signup.
- **Task Management**: CRUD operations for tasks.
- **Task Assignment**: Assign tasks to users.
- **Task Filters & Sorting**: Search, status, and priority filters.
- **File Upload**: Attach files to tasks.
- **Real-Time Updates**: WebSockets for instant changes.
- **Dashboard & Analytics**: Visual representation of tasks.
- **User Management**: Manage users and teams.
- **Responsive UI**: Use Ant Design and Tailwind CSS.
- **Testing & Deployment**: Automated tests and GitHub Pages deployment.

## 🎯 Core Features

1. **User Authentication**
   - Login & Logout (Mocked initially, backend later)
2. **Task Management**
   - Add, Edit, Delete, and View tasks
   - Set Priority & Due Dates
3. **Task Status Tracking**
   - Drag-and-drop Kanban board
   - Filter tasks by status, priority
4. **User Notifications (Future)**
   - Reminders for due tasks
5. **Analytics & Reports (Future)**
   - Task completion trends

## 📌 Non-Functional Requirements

- **Scalability:** Modular component-based architecture
- **Performance:** Optimized React rendering
- **Testing:** TDD-driven development

## 🚀 Development Phases

### Phase 1: Frontend-Only

- Use mock data (or local storage) for tasks and user data.
- Build full UI components and implement state management, routing, and interactions.
- Implement all core features.
- Ensure the app is responsive and well-styled.
- Use the latest React (v19.0.0) and React Router DOM (v7.1.5).

### Phase 2: Backend Integration

- Replace mock data with API calls to a backend service.
- Integrate authentication, persistent storage, and real-time updates.
- Migrate state and data management from mock/local to remote APIs.

<!-- ## 📂 Folder Structure
📂 tms
┣ 📂 src
┃ ┣ 📂 components
┃ ┃ ┣ 📜 TaskList.js
┃ ┃ ┣ 📜 TaskForm.js
┃ ┣ 📂 pages
┃ ┃ ┣ 📜 Dashboard.js
┃ ┃ ┣ 📜 Login.js
┃ ┣ 📂 context
┃ ┃ ┣ 📜 AuthContext.js
┃ ┣ 📂 services
┃ ┃ ┣ 📜 api.js
┃ ┃ ┣ 📜 websocket.js
┃ ┣ 📜 App.js
┣ 📜 package.json
┣ 📜 index.js

tms/
├── docs/
│ ├── 01_Requirements.md
│ ├── 02_Screens.md
│ ├── 03_Features.md
│ ├── 04_Technical_Stack.md
│ ├── 05_Development_Plan.md
│ ├── 06_Testing_Strategy.md
│ └── 07_Deployment.md
├── public/
└── src/
├── components/
├── context/
├── pages/
├── services/
├── App.js
└── index.js -->

## 📝 Note

- The initial phase will use **mock data** and/or **localStorage** to simulate task persistence.
- Future updates (Phase 2) will integrate a backend API and real-time features.
