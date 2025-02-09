# 📌 Development Plan

## Phase 1: Frontend-Only Development

- [ ] **Project Setup**
   - [X] Initialize project with Vite.
     - [X] run `npm create vite@latest ./`
   - [X] Configure ESLint, Prettier, Tailwind CSS, and Ant Design.
     - [X] Configure ESLint & Prettier 
       - [X] run `npm install -D eslint prettier eslint-plugin-react eslint-config-prettier eslint-plugin-prettier`
       - [X] Update `.eslint.config.js` for TypeScript + React + Prettier
       - [X] run `npm run lint` to find linting errors
       - [X] run `npm run lintfix` to fix linting errors, update `.eslint.config.js` if required to handle certain rules
   - [ ] Set up basic folder structure.
- [ ] **Authentication (Mock)**
   - [ ] Create a simulated login (using Auth Context) for Google OAuth.
   - [ ] Protect routes with a custom `<ProtectedRoute>` component.
- [ ] **Task Management**
   - [ ] Build Task CRUD functionality using mock data/localStorage.
   - [ ] Create components: `TaskList`, `TaskForm`, `TaskDetails`.
   - [ ] Implement state management (using Redux Toolkit or Zustand).
- [ ] **Routing**
   - [ ] Set up routing using React Router DOM v7.
   - [ ] Define routes for Login, Dashboard, Task Details, etc.
- [ ] **UI & Styling**
   - [ ] Use Ant Design and Tailwind CSS to style components.
   - [ ] Ensure responsiveness across devices.
- [ ] **Basic Analytics & Filtering**
   - [ ] Add filtering (by status, priority) and sorting for tasks.
   - [ ] Display simple charts or summaries in the Dashboard.
- [ ] **Testing & Quality Assurance**
   - [ ] Write unit tests for components (Jest, React Testing Library).
   - [ ] Add integration tests for user flows.
   - [ ] (Optional) Use Cypress for end‑to‑end tests.
- [ ] **Deployment (Frontend Only)**
   - [ ] Deploy the frontend on GitHub Pages.

## Phase 2: Backend Integration (Future Phase)

- [ ] **Backend Setup**
   - [ ] Choose a backend framework and set up a REST/GraphQL API.
- [ ] **API Integration**
   - [ ] Replace mock data calls with API requests using Axios or Fetch.
   - [ ] Update state management to reflect API data.
- [ ] **Authentication Integration**
   - [ ] Replace simulated login with real authentication (Firebase/Auth0).
- [ ] **Real-Time Updates**
   - [ ] Integrate WebSockets for live notifications and task updates.
- [ ] **Enhanced Features**
   - [ ] Add file uploads, advanced analytics, and user management.
- [ ] **Testing**
   - [ ] Update tests to account for asynchronous API calls.
