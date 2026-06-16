# 32 Puzzle Games — Vercel deployment

This repository contains a static collection of 32 browser games inside the `games/` folder.

What I changed to make Vercel deployment smooth:

- Added a root `vercel.json` that rewrites requests to the `games/` folder.
- Added a `<base href="/games/">` tag to `games/index.html` so relative links and iframe sources resolve correctly when visiting `/`.

How to deploy on Vercel (recommended):

1. Push these changes to your Git remote (e.g., `main` branch):

```bash
git add .
git commit -m "Add Vercel config and deployment README"
git push origin main
```

2. Create a new project on Vercel and import this Git repository. No build command is required — Vercel will serve the static files.

3. Alternatively, deploy from the CLI:

```bash
npx vercel --prod
```

If you want me to also remove the existing `games/vercel.json` (it's safe to keep but redundant), or to move files into a different layout, tell me and I will update the repo.
