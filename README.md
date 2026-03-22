# Friendkeeper — Setup Guide

## Step 1: Put it on GitHub Pages (free hosting)

This gives you a URL like `https://yourname.github.io/friendkeeper` that works on any device.

1. Go to **github.com** and create a free account if you don't have one
2. Click the **+** icon (top right) → **New repository**
3. Name it `friendkeeper`, make it **Public**, click **Create repository**
4. Click **uploading an existing file** (link in the middle of the page)
5. Drag your `index.html` file onto the page → click **Commit changes**
6. Go to **Settings** (tab at the top of your repo) → click **Pages** in the left sidebar
7. Under "Branch", select **main** → click **Save**
8. Wait 1–2 minutes, then your app is live at:
   `https://YOUR-USERNAME.github.io/friendkeeper`

**On your iPhone:** Visit that URL in Safari → tap the Share icon → **Add to Home Screen**. It'll appear as an app icon.

---

## Step 2: Connect Google Drive (cloud backup)

This lets your notes sync to a file in your Google Drive so they're never lost.

### Create a Google Cloud project (free, ~5 minutes)

1. Go to **console.cloud.google.com** and sign in with your Google account
2. Click **Select a project** (top left) → **New Project**
3. Name it `Friendkeeper` → click **Create**
4. In the search bar, search for **"Google Drive API"** → click it → click **Enable**

### Get your API Key

1. In the left menu, go to **APIs & Services** → **Credentials**
2. Click **+ Create Credentials** → **API Key**
3. Copy the key that appears (starts with `AIza…`) — paste it somewhere safe

### Get your Client ID

1. Click **+ Create Credentials** → **OAuth client ID**
2. If prompted, click **Configure consent screen** first:
   - Choose **External** → fill in just the App Name (`Friendkeeper`) and your email → Save
3. Back in Create OAuth client ID:
   - Application type: **Web application**
   - Name: `Friendkeeper`
   - Under **Authorized JavaScript origins**, add:
     `https://YOUR-USERNAME.github.io`
   - Click **Create**
4. Copy the **Client ID** (ends in `.apps.googleusercontent.com`)

### Connect in the app

1. Open Friendkeeper on your phone or computer
2. Tap the **☁️ Sync** button → **Set up Google Drive sync**
3. Paste your API Key and Client ID → tap **Connect**
4. Sign in with your Google account when prompted
5. That's it — tap **☁️ Sync** any time to save your notes to Google Drive

### What gets saved?
A single file called `friendkeeper-data.json` will appear in your Google Drive. You can see it, download it, or delete it at any time.

---

## Updating the app in the future

If you get an updated `index.html` from Claude:
1. Go to your GitHub repo
2. Click on `index.html` → click the pencil ✏️ icon → paste in the new code → **Commit changes**
3. The live site updates automatically within a minute or two
