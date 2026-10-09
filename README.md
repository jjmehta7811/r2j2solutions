# R2J2 Solutions website
Static site for r2j2solutions.com. Every push to `main` auto-deploys via GitHub Pages (.github/workflows/deploy.yml).
Edit index.html / assets/, commit, push -> live in ~1 minute.

## One-time setup
1. Create an empty GitHub repo (e.g. r2j2solutions-site), then in this folder:
   git init -b main && git add -A && git commit -m "Initial site" && git remote add origin <repo-url> && git push -u origin main
2. GitHub repo > Settings > Pages > Source: "GitHub Actions"; Custom domain: r2j2solutions.com; tick Enforce HTTPS.
3. GoDaddy > DNS for r2j2solutions.com: delete the parking A record/forwarding, then add
   A @ 185.199.108.153 / 185.199.109.153 / 185.199.110.153 / 185.199.111.153
   CNAME www <your-github-username>.github.io
