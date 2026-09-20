# Taskflow — CodeAlpha Project Management Tool

A responsive Trello-inspired full-stack project board.

## Features
- JWT authentication and bcrypt password hashing
- Create and view project workspaces
- Invite existing users to a project by email
- Kanban columns: To do, In progress, Done
- Create tasks with descriptions, priority, due date, and assignee
- Update task status, delete tasks (project owner), and comment on tasks
- Filter tasks assigned to the signed-in user
- MongoDB persistence and REST API

## Run locally
Requirements: Node.js 18+ and MongoDB.
1. `npm install`
2. Copy `.env.example` to `.env`.
3. Set a strong random `JWT_SECRET` and your `MONGO_URI`.
4. Start MongoDB.
5. Run `npm run dev`.
6. Open http://localhost:5001

## API
- `POST /api/auth/register`, `POST /api/auth/login`
- `GET /api/users`
- `GET/POST /api/projects`
- `GET/PATCH /api/projects/:id`
- `POST /api/projects/:id/members`
- `POST /api/projects/:id/tasks`
- `PATCH/DELETE /api/projects/:id/tasks/:taskId`
- `POST /api/projects/:id/tasks/:taskId/comments`
- `GET /api/health`

Authenticated endpoints require `Authorization: Bearer <token>`.

## Notes
This is an internship learning project, not a production SaaS. Invited teammates must register first. Real-time updates and push notifications are not included in this core version. For production, add rate limiting, stronger validation, secure cookie sessions, audit logging, and tests. Do not commit `.env`.

Suggested GitHub repository: `CodeAlpha_ProjectManagementTool`.
