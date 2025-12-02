# Arcadia — Gaming Portal (Submission Package)

This package contains:
- `homepage/index.html` — the portal home page (link to the game).
- `game/index.html` — a simple HTML5 Canvas game "Cosmo Catch".
- `README.md` — this file with step-by-step instructions.

---

## Goal / Deliverables expected by your assignment

1. Create a home page for your website (gaming portal) and host it on GitHub Pages.
2. Create a GitHub repository and share the repository with multiple users (add collaborators).
3. Develop any game and share the link on your website (game should be hosted on a cloud service — GitHub Pages, Netlify, Vercel, etc. qualify).

---

## Option A — Deploy everything (portal + game) to a single GitHub repository using GitHub Pages

This is the simplest method and meets the requirements: host a site and a game using GitHub Pages (a cloud-hosting option).

1. Create a new repository on GitHub (via web):
   - Name it e.g. `arcadia-portal`
   - Choose **Public**
   - Do NOT initialize with README (optional)

2. From your local machine, run:
```bash
# from inside the folder containing this package (where 'homepage' and 'game' are)
git init
git branch -M main
git add .
git commit -m "Initial portal + game upload"
git remote add origin https://github.com/<YOUR_USERNAME>/arcadia-portal.git
git push -u origin main
```

3. Enable GitHub Pages:
   - Go to repository → Settings → Pages
   - Under "Source" choose branch `main` and folder `/ (root)` or `/docs` if you placed files there.
   - Save — after a minute your site will be served at:
     `https://<YOUR_USERNAME>.github.io/arcadia-portal/`

4. Verify:
   - Visit the URL and click **Play Game**. If you used root, the play link `./game/index.html` will open your game.

---

## Option B — Host game separately (recommended if you want the game as a standalone cloud app)

1. Create two repos: `arcadia-portal` (homepage) and `cosmo-catch` (game).
2. Deploy `arcadia-portal` to GitHub Pages as above.
3. Deploy `cosmo-catch` to GitHub Pages similarly (it will be available at `https://<YOUR_USERNAME>.github.io/cosmo-catch/`).
4. Edit `homepage/index.html` and change the Play Game link to the published game URL.

---

## Sharing the repository with multiple users (adding collaborators)

1. On GitHub, open your repository page.
2. Click **Settings** → **Manage access** → **Invite a collaborator**.
3. Enter the collaborator's GitHub username or email and send invitation.
4. They will receive an invite to accept; once accepted they can push/pull depending on permissions.

For organizations, you can add team members or use `Settings → Collaborators & teams`.

---

## Alternative cloud hosts (Netlify / Vercel)

- Netlify: drag and drop the `homepage` folder in Netlify UI or connect repo to Netlify for automatic deploys.
- Vercel: connect GitHub repo and deploy — choose the root folder or `homepage` as the output.

---

## Example replacement strings you must change
- Replace `https://github.com/<YOUR_USERNAME>/arcadia-portal.git` with your actual repo URL.
- After enabling Pages, replace the play button href in `homepage/index.html` to your published game URL.

---

## Grading checklist (what to submit to your instructor)
- Code files (you can zip them) — included in this package.
- GitHub repo link for the portal (example): `https://github.com/<YOUR_USERNAME>/arcadia-portal`
- GitHub Pages URL for the portal (example): `https://<YOUR_USERNAME>.github.io/arcadia-portal/`
- GitHub repo link for the game (if hosted separately): `https://github.com/<YOUR_USERNAME>/cosmo-catch`
- Game guest link (cloud URL): `https://<YOUR_USERNAME>.github.io/cosmo-catch/` (or Netlify/Vercel link)
- List of collaborators (usernames or GitHub profiles) that you added.

---

## Notes / Troubleshooting
- If your site shows 404 after enabling Pages: wait a minute and hard refresh. Ensure files are committed to main branch.
- If you want the portal at a custom domain, configure it via repository Pages settings.
- If you need me to provide the exact `index.html` edited for a published URL, paste your published game URL here and I'll provide a ready-to-commit replacement.

Good luck! — If you want, I can:
- Generate a ready `CNAME` file for a custom domain
- Provide a `gh-pages` deployment script (npm) or a GitHub Actions workflow to auto-deploy
