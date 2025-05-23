# Redis Setup (Secure & PCI Compliant)

## 📌 Overview
Configured Redis server for caching and in-memory operations in PCI DSS scoped environment. Ensured secure authentication and minimal exposure.

## ⚙️ Configuration Steps
1. Created Redis EC2 instance (Ubuntu).
2. Installed Redis via APT package.
3. Configured Redis to run as a background service.
4. Bound Redis only to localhost/IP using `bind` directive.
5. Disabled protected-mode.
6. Enabled password authentication (`requirepass`).
7. Configured Redis to start on system boot.

## 🔐 Security Configuration
- 🔒 Enabled password-based authentication.
- 🧱 UFW (firewall) enabled: only whitelisted internal IPs allowed.
- 🔐 Config file permissions restricted to root.
- 📁 Redis logs stored securely with restricted access.

## 📄 Redis Config Highlights
```bash
bind 127.0.0.1
protected-mode no
requirepass "StrongPasswordHere!"
logfile /var/log/redis/redis-server.log
