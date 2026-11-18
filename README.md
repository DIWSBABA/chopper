# Chopper's Little World

A responsive shared-pet website starter, made for GitHub Pages. The included version runs in local-only mode (each browser/device has its own save). For true shared live sync between you and your girlfriend, configure Firebase Realtime Database.

## Publish on GitHub Pages
1. Sign in at https://github.com and click **New repository**.
2. Repository name: `choppers-little-world`. Set it to **Public**.
3. Upload all files from this folder (index.html, style.css, app.js, assets/). Do not upload the parent folder wrapper.
4. Open **Settings → Pages**.
5. Under Build and deployment, choose **Deploy from a branch**, select `main` and `/ (root)`, then Save.
6. After a minute, your URL will look like `https://YOUR-USERNAME.github.io/choppers-little-world/`.

## Live sync (both see each other's actions)
The bundled starter currently stores progress in the browser's localStorage, so it is not yet shared across devices. To enable real-time shared state, connect Firebase Realtime Database:
1. Create a project at https://console.firebase.google.com and add a Web app.
2. Enable **Realtime Database** (choose a European region if offered).
3. Copy the Firebase web config into `firebase-config.js` (create this file from the template in the next step).
4. In database Rules, use authenticated access for production. Do not leave the database publicly writable. This starter has no sign-in yet, so secure cross-device sharing requires adding Firebase Authentication (for example, anonymous auth) and database rules restricting writes to your shared pet.

