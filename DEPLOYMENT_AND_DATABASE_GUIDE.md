# Production Deployment & Database Setup Guide (Firebase, Supabase, Vercel, or Node.js)

Instead of embedding HTML inside Google Sites (which runs in a restricted iframe without a database), deploy this web application directly as a standalone web app with **Gmail / Email login** and a **Cloud Database**.

## Option 1: Firebase Hosting + Google/Gmail Auth + Cloud Firestore (Recommended — 100% Free Tier)

1. Go to the [Firebase Console](https://console.firebase.google.com/) and click **Create a project**.
2. **Enable Gmail & Email Login:**
   - Go to **Build → Authentication → Get started → Sign-in method**.
   - Enable **Google** (Gmail one-click login) and **Email/Password**, then click **Save**.
3. **Enable Cloud Firestore Database:**
   - Go to **Build → Firestore Database → Create database** (start in production mode).
   - In the **Rules** tab, paste the contents of `firestore.rules` so each logged-in user can read/write their own `users/{userId}` document.
4. **Connect Your Web App:**
   - Go to **Project Overview → Project settings → Your apps → Web (`</>`)**, register the app, and copy the `firebaseConfig` object.
   - Open your web app, click **Sign In / Account → Database Setup (Firebase / Supabase / API)**, and paste your `firebaseConfig` JSON (or paste it into `DEFAULT_FIREBASE_CONFIG` in `website/index.html`).
5. **Host on Vercel, Netlify, GitHub Pages, or Firebase Hosting:**
   - **Vercel / Netlify:** Import your GitHub repository `avvadukkam/SDE-Interview-and-Prep-Roadmap-Tracker` at [vercel.com](https://vercel.com) or [netlify.com](https://www.netlify.com) (`vercel.json` and `netlify.toml` are already configured!). Add your domain under **Firebase Console → Authentication → Settings → Authorized domains**.
   - **Firebase Hosting:** Run `firebase deploy` from the repository root (`firebase.json` is pre-configured).

## Option 2: Supabase Auth (Google + Email) + PostgreSQL Database

1. Create a free project at [supabase.com](https://supabase.com).
2. Open the **SQL Editor** and run `supabase/schema.sql` to create the `public.user_progress` PostgreSQL table with Row-Level Security.
3. Under **Authentication → Providers**, enable **Email** and **Google**.
4. Copy your **Project URL** and **anon public key** from **Project Settings → API** and paste them into the app's **Database Setup → Supabase PostgreSQL** tab.

## Option 3: Self-Hosted Node.js + Express + SQLite Database (`backend/server.js`)

1. Run locally or deploy `backend/` to Render, Railway, or Fly.io:
   ```bash
   cd backend
   npm install
   npm start
   # Opens full-stack app + SQLite database at http://localhost:8080
   ```
