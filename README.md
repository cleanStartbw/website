# CleanStart Botswana

Static cleaning-service website, ready to upload to GitHub and deploy on Vercel.
The supplied design and content are preserved in `public/index.html`.

## Files

- `public/index.html`: complete website, including CSS and SVG artwork.
- `vercel.json`: serves the public folder without a build or dependency installation.
- `.gitignore`: excludes local settings and secrets from Git.

No npm installation, API keys, environment variables, or backend are required.
Google Fonts loads online; system fonts are used when unavailable. Quote buttons
open WhatsApp at **+267 77 749 858**. The site does not collect bookings itself.

## Upload to GitHub (no terminal needed)

1. Extract the ZIP on your computer.
2. Create a GitHub repository named `cleanstart-botswana`.
3. Use **uploading an existing file** on the empty repository page, or
   **Add file → Upload files** on an existing repository.
4. Upload the contents of the extracted `cleanstart-botswana` folder. Keep
   `public` as a folder. `vercel.json` and `README.md` must be at the repository
   root, not inside an extra `cleanstart-botswana` folder.
5. Include `.gitignore` if your file browser shows hidden files, then commit.

Upload the extracted files, not the ZIP itself.

## Deploy on Vercel

1. Go to https://vercel.com/new and connect your GitHub account.
2. Import the `cleanstart-botswana` repository.
3. Select **Other** as the Framework Preset if asked.
4. Keep Root Directory at the repository root (`./`). The included
   `vercel.json` sets Output Directory to `public` and leaves Build Command
   and Install Command empty. No environment variables are needed.
5. Click **Deploy**, then open the deployment URL.

After connecting GitHub, commits to the production branch trigger deployments.
Add a custom domain later in the project's **Settings → Domains**.

## Preview locally

Open `public/index.html` directly in your browser. Alternatively, with Python:

```sh
python -m http.server 8000 --directory public
```

Then open http://localhost:8000.

## Edit content

Edit `public/index.html` and commit the changes to GitHub.

- Contact: replace every occurrence of `26777749858` to change WhatsApp number.
- Prices: search for `P250`, `P350`, `P500`, and `P400`.
- Colours, layout and fonts: edit the `<style>` block near the top.
- Copyright: the footer currently says 2026.

Before sharing the live URL, confirm the business number and prices, check the
page on a phone, and click the quote buttons to confirm the WhatsApp destination.

## Optional Git terminal workflow

Create an empty GitHub repository first, then run these commands from this folder.
Replace YOUR_USERNAME with your actual GitHub username.

```sh
git init -b main
git add .
git commit -m "Prepare CleanStart Botswana website"
git remote add origin https://github.com/YOUR_USERNAME/cleanstart-botswana.git
git push -u origin main
```

## Deployment references

- https://vercel.com/docs/project-configuration
- https://vercel.com/docs/git/vercel-for-github

This package has been prepared for deployment; no GitHub repository or live
Vercel deployment has been created as part of this package.
