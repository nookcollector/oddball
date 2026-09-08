# oddball.works

https://oddball.works — repo: nookcollector/oddball

AI-native creative studio site. Single static page — no build step.

## Structure
- `index.html` — the whole site (Work / About / Contact + 7 case pages, hash routing)
- `img/` — case images and logo

## Local preview
Open `index.html`, or:
```
npx serve .
```

## Deploy (Vercel)
1. Push this folder to a GitHub repo.
2. vercel.com → Add New Project → import the repo.
3. Framework Preset: **Other**. Build Command: empty. Output Directory: `.` (or `site` if you push the whole project).
4. Deploy, then Settings → Domains → add your domain.
5. At your registrar, set DNS for **oddball.works**:
   - `A` `@` → `76.76.21.21`
   - `CNAME` `www` → `cname.vercel-dns.com`
   (Vercel shows the exact values under Settings → Domains; use those if they differ.)

HTTPS is issued automatically.

## Notes
- Case videos are YouTube embeds (click-to-play), so nothing heavy is served from this repo.
- Portfolio (text index + hover preview) is kept commented out in `index.html`, marked `PORTFOLIO — kept for later use`.
