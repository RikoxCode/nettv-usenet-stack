# 📦 Automated Usenet Media Stack (Radarr · Sonarr · Prowlarr · SABnzbd · Jellyseerr)

A clean, fully automated **Usenet media management stack** using Docker Compose.
Designed for **movies, series, anime**, and **family-friendly requests** via Jellyseerr.

This setup use
- **Eweka** as Usenet provider
- **NZBGeek** as indexer (managed centrally via Prowlarr)
- **NAS-mounted media directories**
- **Jellyseerr** as a request frontend for family & friends

---

## 🧩 Included Services

| Service      | Purpose |
|--------------|--------|
| **Prowlarr** | Indexer management (NZBGeek, syncs to Radarr/Sonarr) |
| **SABnzbd**  | Usenet downloader (Eweka configured here) |
| **Radarr**   | Movie management (normal + anime movies) |
| **Sonarr**   | Series management (normal + anime series) |
| **Jellyseerr** | User-friendly request UI (family-safe frontend) |

---

## 📁 NAS Folder Layout (Required)

Your NAS **must already be mounted** at `/mnt/nas-media` on the Docker host.

```text
/mnt/nas-media/
├── movies
├── series
├── anime/
│   ├── movies
│   └── tv
```

---

## 🚀 Getting Started

```bash
# Enter stack folder
cd nettv-usenet-stack

# Start docker-stack in background
docker compose up -d
```

---

## 🌐 Web Interfaces

| Service | URL |
|-------|-----|
| SABnzbd | http://localhost:8080 |
| Radarr | http://localhost:7878 |
| Sonarr | http://localhost:8989 |
| Prowlarr | http://localhost:9696 |
| Jellyseerr | http://localhost:5055 |

---

## 🔒 Security

Do **not** expose services directly to the internet.
Use VPN or a reverse proxy with authentication.

---
