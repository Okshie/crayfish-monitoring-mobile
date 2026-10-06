# Crayfish Monitoring Mobile — GitHub Pages

This package is flattened and ready to upload to the **root of the `main` branch** of a GitHub repository.

## Files
- `index.html` — mobile dashboard
- `login.html` — mobile login page
- `config.js` — Supabase project URL, publishable key, and device ID
- `manifest.webmanifest` — PWA manifest
- `sw.js` — service worker
- `404.html` — GitHub Pages fallback
- `.nojekyll` — prevents unnecessary Jekyll processing

## GitHub Pages
1. Upload **all files in this folder directly into the repository root**. Do not upload the containing folder itself.
2. In **Settings → Pages**, choose **Deploy from a branch**.
3. Select branch **main** and folder **/(root)**, then Save.
4. The project site URL is `https://<your-github-username>.github.io/<repository-name>/`.

For the repository shown in the original project, that pattern is `https://okshie.github.io/crayfish-monitoring-mobile/`.

The mobile app now uses `./login.html` instead of `../website/login.html`, so it no longer depends on a separate `website/` directory.

## Supabase
Make sure the Supabase Auth user exists and that the database RLS policies allow the authenticated user to read/write the tables used by the dashboard.
