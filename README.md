# Akshat Challenge — Backend API

This project contains a simple backend API that runs on **Port 80** and exposes a single route `/sayHello`.

## ✅ Route
**GET** `/sayHello`

**Response**
```json
{ "message": "Hello User" }
```

## ⚙️ Setup
```bash
npm install
sudo node server.js
```

Then visit: `http://localhost/sayHello`

## 🚀 Deployment (via GitHub Actions)
Every push to the `main` branch triggers the workflow `.github/workflows/deploy.yml`, which:
- SSHes into the provided Azure VM.
- Uploads code to `/home/azureuser/akshat-app`.
- Installs dependencies and runs the app on Port 80.

## 🧷 GitHub Secret
- `VM_KEY` → contents of the provided PEM file.

## 🧪 Testing
After deployment:
```bash
curl http://4.246.142.4/sayHello
```

Expected output:
```json
{ "message": "Hello User" }
```
