# 📌 Screen-wise Plan – Task Management System (TMS)

## Overview

The app is a single‑page application with multiple “views” using React Router DOM v7.1.5.

## Screens & Components

| **Screen**          | **Features**                                                        | **Components / Files**                    |
| ------------------- | ------------------------------------------------------------------- | ----------------------------------------- |
| **Login Page**      | User authentication via Google OAuth (frontend mock initially)      | `Login.js`, `AuthContext.js`              |
| **Dashboard**       | Overview of tasks, status filters, summary analytics                | `Dashboard.js`, `TaskList.js`, `Stats.js` |
| **Task Creation**   | Form for adding a new task (with validation)                        | `TaskForm.js`, `Validation.js`            |
| **Task Details**    | View, edit, and delete a task; file attachment (mocked file upload) , status updates          | `TaskDetails.js`, `FileUpload.js`         |
| **User Management** | (Optional for frontend phase) View list of users and assign tasks   | `UserList.js`, `AssignTask.js`            |
| **Settings**        | User profile settings and logout                                    | `Settings.js`                             |
| **Notifications**   | (Advanced feature for Phase 2) Real‑time updates via WebSockets     | `WebSocketService.js` (stub/mock version) |

## Navigation Flow

1. **Login**: The user logs in (using Google OAuth or a simulated login) and is directed to the Dashboard.
2. **Dashboard**: Displays a list of tasks, filtering options, and an analytics summary.
→ Users can:
   - View task lists.
   - Click on a task to **view details**.
   - Click **Add Task** to create a new one.
3. **Task Creation & Details**: Users can create a new task or select an existing one to view details and edit.
4. **User Management Page** → Admins can assign tasks.
5. **Settings Page** → Users can change settings and log out.
