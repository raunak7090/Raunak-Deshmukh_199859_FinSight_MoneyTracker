# FinSight MoneyTracker – Monorepo

This repository contains two separate frontend projects:

- **Money Tracker** – Next.js finance tracker with Firebase + AI insights  
  Location: `Money Tracker/`
- **Insightful Wallets** – Vite + React + TypeScript dashboard  
  Location: `insightful-wallets/`

Both are Node.js projects managed with `npm`.

---

## ⚙️ Prerequisites

- **Node.js** `>= 18` (required by Money Tracker)
- **npm** (comes with Node.js)
- Git (for cloning the repository)

Check versions:

```bash
node -v
npm -v
```

---

## 📁 Project Structure

```text
.
├── Money Tracker/        # Next.js app (personal finance tracker)
└── insightful-wallets/   # Vite + React app (Insightful Wallets dashboard)
```

---

## 🚀 Getting Started

## 📌 Running **Money Tracker** (Next.js + Firebase)

Project path: `Money Tracker/`

### 1. Install Dependencies

```bash
cd "Money Tracker"
npm install
```

### 2. Run in Development

```bash
npm run dev
```

By default, Next.js runs at:

- http://localhost:3000

### 4. Build & Start (Production)

```bash
npm run build
npm start
```

---

## 📌 Running **Insightful Wallets** (Vite + React + TS)

Project path: `insightful-wallets/`

### 1. Install Dependencies

```bash
cd insightful-wallets
npm install
```

### 2. Run in Development

```bash
npm run dev
```

Vite will show the dev server URL, commonly:

- http://localhost:5173 or http://localhost:8080 (see terminal output)

### 4. Build & Preview

```bash
# build
npm run build

# optional: preview production build
npm run preview
```

---

## 🔗 Running Both Projects Together

You can run both apps in separate terminals:

1. **Terminal 1 – Money Tracker**

   ```bash
   cd "Money Tracker"
   npm run dev   # http://localhost:3000
   ```

2. **Terminal 2 – Insightful Wallets**

   ```bash
   cd insightful-wallets
   npm run dev   # http://localhost:5173 (or similar)
   ```

If Insightful Wallets should talk to the Money Tracker backend/API:

- Make sure your backend is on `http://localhost:3000` (or adjust `VITE_API_BASE_URL` accordingly).
