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

### 1. Clone the Repository

```bash
git clone https://github.com/raunak7090/Raunak-Deshmukh_199859_FinSight_MoneyTracker.git
cd Raunak-Deshmukh_199859_FinSight_MoneyTracker
```

---

## 📌 Running **Money Tracker** (Next.js + Firebase)

Project path: `Money Tracker/`

### 1. Install Dependencies

```bash
cd "Money Tracker"
npm install
```

### 2. Environment Variables

There is a `.env.local.example` file with all required environment keys for Firebase.

Create your own `.env.local`:

```bash
cp .env.local.example .env.local   # on Windows PowerShell: copy .env.local.example .env.local
```

Fill in values:

```env
NEXT_PUBLIC_FIREBASE_API_KEY=your_api_key
NEXT_PUBLIC_FIREBASE_AUTH_DOMAIN=your_project.firebaseapp.com
NEXT_PUBLIC_FIREBASE_PROJECT_ID=your_project_id
NEXT_PUBLIC_FIREBASE_STORAGE_BUCKET=your_project.appspot.com
NEXT_PUBLIC_FIREBASE_MESSAGING_SENDER_ID=your_sender_id
NEXT_PUBLIC_FIREBASE_APP_ID=your_app_id

FIREBASE_ADMIN_PROJECT_ID=your_project_id
FIREBASE_ADMIN_CLIENT_EMAIL=firebase-adminsdk-xxxxx@your_project.iam.gserviceaccount.com
FIREBASE_ADMIN_PRIVATE_KEY="-----BEGIN PRIVATE KEY-----\n...\n-----END PRIVATE KEY-----\n"
```

### 3. Run in Development

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

### 2. Environment Variables (Optional / Backend Integration)

The frontend reads:

- `VITE_API_BASE_URL` – API base URL (defaults to `http://localhost:3000` if not set)
- `VITE_FIREBASE_API_KEY` – used for token refresh with Firebase

Create a `.env` file in `insightful-wallets/` if needed:

```env
VITE_API_BASE_URL=http://localhost:3000
VITE_FIREBASE_API_KEY=your_firebase_web_api_key
```

> If you run a custom backend, point `VITE_API_BASE_URL` to your backend URL.

### 3. Run in Development

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
