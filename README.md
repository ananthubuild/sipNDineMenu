# Sip N Dine Menu

Full-screen PDF viewer. No UI — only the menu.

Live site: **https://sipndinemenu.web.app**

## Automatic deploy (GitHub Actions)

Every push to `main` deploys to Firebase Hosting.

### One-time setup (required once)

1. Open [Firebase Console → sipndinemenu → Project settings → Service accounts](https://console.firebase.google.com/project/sipndinemenu/settings/serviceaccounts/adminsdk).
2. Click **Generate new private key** and save the JSON file.
3. In GitHub: [ananthubuild/sipNDineMenu → Settings → Secrets and variables → Actions](https://github.com/ananthubuild/sipNDineMenu/settings/secrets/actions).
4. Click **New repository secret**:
   - Name: `FIREBASE_SERVICE_ACCOUNT`
   - Value: paste the **entire** contents of the JSON file.
5. Push to `main` — the workflow runs automatically.

Check runs under the **Actions** tab on GitHub.

## Manual deploy

```bash
firebase login
firebase deploy --only hosting
```

## Local preview

Open `public/index.html` in a browser, or run:
```
firebase serve --only hosting
```

## Note

Firebase **Hosting** uses `.firebaserc` (project: `sipndinemenu`). You do **not** need the Firebase JS SDK or Analytics for this site — the PDF is served as a static file.
