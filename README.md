# Coherence Tech

Static site (no build step). `index.html` is the whole site; `assets/` holds the two intro videos and the share image.

## Deploy to Vercel

Option A, Vercel CLI (from this folder):

    npm i -g vercel
    vercel            # first run: answer the prompts (framework: Other, no build command, output directory: .)
    vercel --prod

Option B, GitHub: push this folder to a repo, then in Vercel choose "Add New Project", import the repo,
Framework Preset "Other", leave Build Command empty, Output Directory ".".

## Things to fill in

- Contact email: `CONFIG.EMAIL` near the top of the script in `index.html` (currently paraiq.app@gmail.com).
- Work slides: `CONFIG.WORK` in the same place (`[{title, discipline, year, image}]`).
- Intro videos: `CONFIG.INTRO_VIDEO` (landscape and portrait files in `assets/`). Set it to `null` to turn the intro off.
- Share image: after you have a domain, change `og:image` in the head of `index.html` to the full URL, e.g. `https://yourdomain.com/assets/og.png`.
