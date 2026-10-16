# Home Task Organizer — Setup Guide

Everything lives in these three files. About 10 minutes, one time only.

## 1. Get a Firebase project

- Go to [console.firebase.google.com](https://console.firebase.google.com)
- Use the Google account you already have. Either select your existing project or click **Add project** and follow the prompts (Google Analytics: not needed — you can skip it).

## 2. Add a Web app and copy the config

- In your project, click the **gear icon → Project settings** (top left).
- Scroll to **Your apps** → click the **`</>`** (Web) icon.
- Give it a nickname like `home-organizer`, then **Register app**.
- You'll see a `firebaseConfig` object. In `she-home-organizer.html`, find the block marked **`FIREBASE_CONFIG`** near the top of the `<script>` and paste your values into it (replacing the `PASTE_YOUR_...` placeholders).

## 3. Turn on Anonymous sign-in

- Left menu → **Build → Authentication** → **Get started** (if you haven't used it before).
- Go to the **Sign-in method** tab → click **Anonymous** → **Enable** → **Save**.
- This is what lets her open the app with zero login — the app signs her in silently in the background.

## 4. Create the Firestore database

- Left menu → **Build → Firestore Database** → **Create database**.
- Choose **Start in production mode**, pick the location closest to you, **Enable**.

## 5. Paste the security rules

- In Firestore Database, open the **Rules** tab.
- Delete what's there and paste the entire contents of **`firestore.rules`** (included next to this file).
- Click **Publish**.
- These rules mean each person can only read/write their own data.

## 6. Put the app on GitHub Pages

- Put `she-home-organizer.html` in your GitHub repository (e.g. rename it to `index.html` if you want it as the site's home page).
- In the repo: **Settings → Pages** → under *Build and deployment*, choose **Deploy from a branch**, pick your branch and folder → **Save**.
- Open the published URL on her phone and **Add to Home Screen** — it'll feel like a real app.

## Backup

Even though everything syncs to Firebase, the app has **Settings → Export backup** (downloads a JSON file) and **Import backup**. Worth doing once in a while — good housekeeping. 💛
