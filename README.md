# YouTube WebView Wrapper for Android

A clean Android WebView wrapper for YouTube with fullscreen video support, pull-to-refresh, and deep link handling. Built to be compiled via GitHub Actions — no PC required.

---

## ✨ Features

- Full YouTube mobile experience (m.youtube.com)
- **Fullscreen video** with immersive mode
- **Pull-to-refresh** with YouTube red indicator
- **Deep link support** — opens youtube.com and youtu.be links directly in the app
- **Hardware-accelerated** WebView
- Cookies & DOM storage for persistent login
- File upload support (for profile pics etc.)
- Dark theme throughout

---

## 🚀 Build via GitHub Actions (No PC needed)

### Step 1 — Create a GitHub repo

1. Go to [github.com](https://github.com) → **New repository**
2. Name it `youtube-wrapper` (or anything you like)
3. Set it to **Public** (free Actions minutes)
4. Click **Create repository**

### Step 2 — Upload the files

Option A — **GitHub web UI** (easiest):
1. In your new repo, click **Add file → Upload files**
2. Drag and drop this entire project folder
3. Click **Commit changes**

Option B — **GitHub mobile app**:
1. Install the GitHub app on your phone
2. Create the repo, then upload files from the app

### Step 3 — Watch the build

1. Go to your repo → **Actions** tab
2. You'll see the workflow `Build YouTube Wrapper APK` running
3. Wait ~3–5 minutes for it to complete ✅

### Step 4 — Download the APK

1. Click on the completed workflow run
2. Scroll down to **Artifacts**
3. Download **YouTubeWrapper-debug** (ready to install)
4. Transfer the APK to your Android phone and install it

> ⚠️ You may need to enable **"Install from unknown sources"** in your phone's settings.

---

## 📦 Project Structure

```
YouTubeWrapper/
├── .github/
│   └── workflows/
│       └── build.yml          ← GitHub Actions CI/CD
├── app/
│   └── src/main/
│       ├── AndroidManifest.xml
│       ├── java/com/ytviewer/
│       │   └── MainActivity.java  ← Main WebView logic
│       └── res/
│           ├── layout/activity_main.xml
│           ├── values/themes.xml
│           └── xml/file_paths.xml
├── build.gradle
├── settings.gradle
└── gradle/wrapper/
    └── gradle-wrapper.properties
```

---

## 🔧 Customization

| What | Where | How |
|------|-------|-----|
| Change start URL | `MainActivity.java` | Edit `YOUTUBE_URL` constant |
| App name | `res/values/strings.xml` | Edit `app_name` |
| Theme color | `res/values/themes.xml` | Edit color values |
| App icon | `res/mipmap-*/` | Replace PNG files |

---

## 📋 Trigger a new build

Any push to `main`/`master` auto-triggers a build. You can also go to **Actions → Build YouTube Wrapper APK → Run workflow** to trigger manually.

To publish a release with APKs attached, push a git tag:
```
git tag v1.0
git push origin v1.0
```
