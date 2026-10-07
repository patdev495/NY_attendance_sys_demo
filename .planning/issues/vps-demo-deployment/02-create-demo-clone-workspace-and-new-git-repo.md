# Issue 02: Create Demo Clone Workspace & Setup Git Repository
Status: ready-for-agent
Type: HITL

## What to build

Clone the project workspace into a clean, dedicated directory `d:\Workspace\Time_Attendance_Machine_Demo` alongside the current workspace. Exclude unnecessary development artifacts (`.venv`, `node_modules`, `.git`, legacy `.tar` image archives, temp files). Configure the cloned workspace for self-contained demo execution by setting `DEMO_MODE=true` in `backend/.env`, updating `docker-compose.yml` to bind port `8060:80`, mounting the freshly generated SQLite snapshot, and initializing a clean Git repository ready to be linked to a new GitHub remote.

## Acceptance criteria

- [ ] Directory `d:\Workspace\Time_Attendance_Machine_Demo` is created containing full application code and assets without virtual environment or node modules bloat.
- [ ] Fresh SQLite snapshot `demo_data/attendance.db` from Issue 01 is present in the demo workspace.
- [ ] Environment file `backend/.env` is configured with `DEMO_MODE=true`.
- [ ] `docker-compose.yml` is configured with port mapping `127.0.0.1:8060:80` for the frontend service.
- [ ] A new Git repository is initialized with an initial commit, ready for the user to add their dedicated GitHub remote URL (`git remote add origin ...`).

## Blocked by

- [Issue 01: Fresh SQLite Data Snapshot Migration](file:///d:/Workspace/Time_Attendance_Machine/.planning/issues/vps-demo-deployment/01-fresh-sqlite-data-snapshot-migration.md)
