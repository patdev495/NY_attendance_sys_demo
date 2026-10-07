# Issue 04: Deploy & Run Docker Compose Demo on VPS
Status: ready-for-agent
Type: AFK

## What to build

Transfer the demo application codebase from `d:\Workspace\Time_Attendance_Machine_Demo` to the target VPS under `/opt/attendance-sys`. Build and start the Docker Compose stack in detached mode. Verify that both backend and frontend containers start reliably, that internal port 8060 binds to `127.0.0.1:8060`, and that the `demo_simulator` service activates without error.

## Acceptance criteria

- [ ] Project files are staged on VPS in `/opt/attendance-sys`.
- [ ] `docker compose build` and `docker compose up -d` execute successfully.
- [ ] Container `time_attendance_frontend` is listening on `127.0.0.1:8060`.
- [ ] Container `time_attendance_backend` starts with `DEMO_MODE=true` and mounts `demo_data/attendance.db`.
- [ ] Container logs verify no crash loops or database connection failures.

## Blocked by

- [Issue 02: Create Demo Clone Workspace & Setup Git Repository](file:///d:/Workspace/Time_Attendance_Machine/.planning/issues/vps-demo-deployment/02-create-demo-clone-workspace-and-new-git-repo.md)
- [Issue 03: Configure VPS Host Nginx Reverse Proxy & Wildcard SSL](file:///d:/Workspace/Time_Attendance_Machine/.planning/issues/vps-demo-deployment/03-configure-vps-host-nginx-reverse-proxy-and-ssl.md)
