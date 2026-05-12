# LUNO PWA — Deployment Guide
**Dr. Ali Mohammed Said · Dar es Salaam, Tanzania**

---

## Files in this package

```
luno-pwa/
├── index.html          ← Entry point (role selector splash screen)
├── owner-app.html      ← Owner dashboard app
├── driver-app.html     ← Driver dashboard app
├── owner-landing.html  ← Owner marketing/landing page
├── driver-landing.html ← Driver marketing/landing page
├── manifest.json       ← PWA manifest (makes it installable)
├── sw.js               ← Service worker (offline support)
├── icons/
│   └── icon.svg        ← App icon (all sizes)
└── README.md           ← This file
```

---

## How to go LIVE in 30 minutes (Free)

### Step 1: Create a GitHub account (if you don't have one)
Go to https://github.com and sign up. Free.

### Step 2: Create a new repository
- Click the green "New" button
- Name it: `luno-app`
- Set to PUBLIC
- Click "Create repository"

### Step 3: Upload all files
- Click "uploading an existing file"
- Drag ALL files from this folder (including the icons/ folder)
- Click "Commit changes"

### Step 4: Enable GitHub Pages
- Go to Settings → Pages
- Under "Source", select: Deploy from branch → main → / (root)
- Click Save
- Wait 2-3 minutes

### Step 5: Your LIVE URL
```
https://YOUR-USERNAME.github.io/luno-app/
```

That's it. LUNO is live on the internet. 🎉
Share this URL on WhatsApp with boda operators in Kariakoo and Ubungo.

---

## How users install LUNO (Android — Chrome)

1. User opens the URL in Chrome
2. They see "Install LUNO" banner at the top
3. They tap "Sakinisha"
4. LUNO appears on their home screen like a real app
5. It works OFFLINE after first visit

## How users install LUNO (iPhone — Safari)

1. User opens the URL in Safari
2. Tap the Share button (box with arrow)
3. Scroll down → tap "Add to Home Screen"
4. Tap "Add"
5. LUNO icon appears on home screen

---

## Custom domain (Optional — makes it professional)

Instead of `github.io/luno-app`, use `app.lunotz.com` or `luno.app`

1. Buy domain at Namecheap (~$10/year) or Hostinger (~$5/year)
2. In GitHub Pages settings, add your custom domain
3. Add a CNAME file to your repo containing: `app.lunotz.com`
4. Update DNS at your registrar with GitHub's IP addresses

---

## Adding icons (PNG versions — needed for full Play Store support)

To generate PNG icons from the SVG:
1. Go to https://realfavicongenerator.net
2. Upload icons/icon.svg
3. Download the generated package
4. Replace icons/ folder contents with the downloaded files
5. Update manifest.json icon paths if needed

---

## Next step after PWA: Capacitor (Android APK)

Once you have 100+ PWA users, convert to a real Android app:

```bash
npm install -g @ionic/cli
npm install @capacitor/core @capacitor/android
npx cap init LUNO com.lunotz.app
npx cap add android
npx cap copy
npx cap open android
```

Then publish to Google Play Store.

---

## Support
**LUNO Project · Dr. Ali Mohammed Said**
Dar es Salaam, Tanzania
