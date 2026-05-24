# Sip N Dine Menu

Full-screen PDF viewer. No UI — only the menu.

## Deploy to Firebase

1. Log in with the Google account that owns **sipndinemenu**:
   ```
   firebase login
   ```
2. From this folder:
   ```
   firebase deploy --only hosting
   ```

Live URL after deploy: **https://sipndinemenu.web.app** (or `.firebaseapp.com`)

## Local preview

Open `public/index.html` in a browser, or run:
```
firebase serve --only hosting
```

## Note

Firebase **Hosting** uses `.firebaserc` (project: `sipndinemenu`). You do **not** need the Firebase JS SDK or Analytics for this site — the PDF is served as a static file.
