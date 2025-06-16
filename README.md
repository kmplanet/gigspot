# GigSpot

A full-stack web application to browse and manage job listings for gig workers and employers. Built with **Vite + TypeScript** on the frontend and **Node.js + Express + MongoDB** on the backend.

---

## 🚀 Project Setup

### 📦 Install Dependencies

From the root directory, install both frontend and backend dependencies:

```bash
npm install
```

This runs:

```bash
cd client && npm install && cd ../server && npm install
```

---

## 🧪 Available Scripts

All commands are run from the root directory:

### Start Production Build

```bash
npm start
```

Runs:
- `npm run build` to build both client and server
- Then concurrently:
  - Starts the frontend with `vite preview`
  - Starts the backend with `node dist/index.js`

### Development Mode (Hot Reload)

```bash
npm run dev
```

Runs concurrently:
- Frontend: `cd client && npm run dev`
- Backend: `cd server && npm run dev`

### Build for Production

```bash
npm run build
```

Compiles:
- Frontend using `vite build`
- Backend using `tsc`

### Clean Project

```bash
npm run clean
```

Removes:
- Node modules
- Compiled files in both `client` and `server`

---

## 🌐 URLs

- Frontend: [http://localhost:4173](http://localhost:4173)
- Backend: [http://localhost:3000](http://localhost:3000)

---

## ⚠️ Common Issues

### MongoDB Not Connected

If you see this error:

```
MongoDB connection error: querySrv ENOTFOUND _mongodb._tcp.cluster0.6eexw.mongodb.net
```

It means the MongoDB URI in your environment config is not resolvable.

**Fix:**

1. Create a `.env` file in the `server/` folder.
2. Add your MongoDB connection string:

```env
MONGODB_URI=mongodb+srv://<username>:<password>@<cluster>.mongodb.net/<db>?retryWrites=true&w=majority
```

---

## 📂 Project Structure

```
GigSpot/
├── client/         # Frontend (Vite + TypeScript)
├── server/         # Backend (Node.js + Express + TypeScript)
├── package.json    # Root scripts
└── README.md       # You’re here!
```

---

## 📌 Notes

- You may see `npm audit` warnings after install. To auto-fix them:

```bash
npm audit fix
```

- To update browser compatibility data:

```bash
npx update-browserslist-db@latest
```

---
