# 📌 Features Breakdown – Task Management System (TMS)

## MVP (Phase 1: Frontend-Only)

1. **User Authentication**
   - Simulated Google OAuth login (frontend mock).
   - Protected routes using Auth Context.
2. **Task Management (CRUD)**
   - Create, read, update, delete tasks.
   - Use mock data or local storage for persistence.
3. **Task Filtering & Sorting**
   - Filter tasks by status (e.g., To Do, In Progress, Completed).
   - Sort by due date, priority, etc.
4. **Task Details**: View/Edit/Delete tasks.
5. **Responsive UI & Styling**
   - Implement using Ant Design and Tailwind CSS.
6. **Routing & Navigation**
   - Use React Router DOM v7 for multi‑page navigation.
7. **Basic Analytics**
   - Simple dashboard graphs or summaries (e.g., number of tasks per status).

## Advanced (Phase 2: Backend Integration)

1. **Backend API Integration**
   - Replace mock data with REST/GraphQL API calls.
2. **Authentication Integration**
   - Use a real authentication provider (e.g., Firebase or Auth0).
3. **Real-Time Updates**
   - Implement WebSockets for live task updates.
4. **File Uploads**
   - Implement file attachment with actual file storage.
5. **Enhanced Analytics & Reporting**
   - Integrate dynamic charts (e.g., using Chart.js or Recharts).
6. **User Management & Role-Based Access**
   - Allow task assignment and admin features.
7. **Notifications**: Users receive task updates.

## 🔧 Technical Considerations

- **Authentication**: Google OAuth via Firebase.
- **State Management**: Redux Toolkit/Zustand.
- **UI Framework**: Ant Design + Tailwind CSS.
- **Performance**: Lazy loading, memoization.
