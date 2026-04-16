# Wingua Terms of Service (GitHub Pages)

Public site for **https://lesymm.github.io/Wingua-terms-of-service/** (default URL used by the Wingua app).

## Create the GitHub repo and push

From this directory (with [GitHub CLI](https://cli.github.com/) installed and authenticated):

```bash
cd Wingua-terms-of-service
git init
git add index.html README.md .gitignore
git commit -m "Add Terms of Service page for Wingua"
gh repo create Wingua-terms-of-service --public --source=. --remote=origin --push
```

If the repo already exists on GitHub:

```bash
git remote add origin https://github.com/lesymm/Wingua-terms-of-service.git
git branch -M main
git push -u origin main
```

Replace `lesymm` with your GitHub username or org if different.

## Enable GitHub Pages

1. On GitHub: **Settings → Pages**
2. **Build and deployment**: Source **Deploy from a branch**
3. Branch **main**, folder **/ (root)**
4. Save. The site will be available at `https://<user>.github.io/Wingua-terms-of-service/` once the build finishes.

## Updating terms

Edit `index.html`, commit, and push. Optionally sync wording from `docs/legal/wingua-terms-of-service.md` in the main Wingua app repo after counsel review.

## Optional EAS override

If the live URL differs, set `EXPO_PUBLIC_TERMS_OF_SERVICE_URL` in Expo / EAS environment variables.
