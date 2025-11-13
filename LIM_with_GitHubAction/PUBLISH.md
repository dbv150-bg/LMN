# 🚀 LIM — Publish Guide

This guide explains how to build and publish your LIM chat app online.

---

## 🧰 Requirements
- A GitHub account  
- LIM repository (this one)  
- GitHub Pages enabled

---

## 🧩 Setup

1. Go to your repo → **Settings → Pages**
2. Under “Build and deployment,” select:
   - **Source:** GitHub Actions
3. Push code to the `main` branch:
   ```bash
   git add .
   git commit -m "Publish LIM"
   git push origin main
   ```

---

## 🌐 Your App URL
After the Action finishes (~2 min):
```
https://<your-username>.github.io/LIM/
```
Open this in Chrome — your **LIM Web App** runs live.

---

## ⚙️ Optional — Deploy Server
If you want a live backend:
1. Create a free VM on [Render](https://render.com) or [Railway](https://railway.app)
2. Push your `server/` folder there
3. Update `client/lib/config.dart` with your live API URL

---

## 💾 Data & Storage
- Chat messages → MongoDB
- Media files → MinIO/S3
- 1.5TB quota can be managed using S3 lifecycle policies.

---

## 🔒 Security
- Use HTTPS everywhere.
- To enable encryption, plug in Signal Protocol (already scaffolded).

---

## 🧹 Maintenance
- `docker compose down` — stop all services locally  
- `docker compose up -d` — restart stack  

---

**Enjoy building LIM 💬**
