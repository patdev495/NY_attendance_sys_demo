# Issue 03: Configure VPS Host Nginx Reverse Proxy & Wildcard SSL
Status: done
Type: AFK

## What to build

Establish the reverse proxy and SSL termination layer on the target VPS (`107.175.144.245`) for domain `attendance-sys.peebot.shop`. Leverage the pre-existing Let's Encrypt wildcard certificate (`/etc/letsencrypt/live/peebot.shop/fullchain.pem`). Create `/etc/nginx/conf.d/attendance-sys.peebot.shop.conf` handling HTTP-to-HTTPS redirection, proxying all inbound traffic to local backend port `127.0.0.1:8060`, and ensuring proper WebSocket headers (`Upgrade`, `Connection`) and timeouts are configured for real-time live attendance monitoring.

## Acceptance criteria

- [x] Configuration file `/etc/nginx/conf.d/attendance-sys.peebot.shop.conf` is deployed on the VPS.
- [x] Port 80 redirects to HTTPS (301) for `attendance-sys.peebot.shop`.
- [x] HTTPS server block uses `/etc/letsencrypt/live/peebot.shop/fullchain.pem` and its private key.
- [x] Reverse proxy passes requests to `http://127.0.0.1:8060` with full WebSocket header forwarding (`$http_upgrade`, `Connection "upgrade"`).
- [x] `nginx -t` validation passes and Nginx service reloads cleanly without downtime for co-hosted websites.

## Blocked by

None - can start immediately.
