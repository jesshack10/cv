# my-project — GitHub Pages demo

This repository demonstrates a Project Site on GitHub Pages.

Publish options:
- Option A (recommended simple): Put your site root in `docs/` on the `main` branch and enable Pages from `main` / `/docs`.
  - Resulting URL: `https://jesshack10.github.io/<repo-name>` (replace `<repo-name>` with your repo).

- Option B: Publish from the `gh-pages` branch. Commit site root to a branch named `gh-pages` and select that as the Pages source.
  - Resulting URL is the same pattern as above.

Notes:
- Add `.nojekyll` if your build produces files/directories starting with an underscore.
- For SSGs (Hugo, Gatsby, Next) you'll usually build locally or with GitHub Actions and publish the generated static files to `docs/` or `gh-pages`.
- If you want a custom domain, add a `CNAME` file with your domain and configure DNS.

## Quick local steps (docs/ approach)
1. mkdir my-project && cd my-project
2. git init
3. mkdir docs && cp ../index.html docs/index.html  # or create docs/index.html
4. git add docs index.html README.md .nojekyll
5. git commit -m "Initial project site"
6. git remote add origin git@github.com:jesshack10/my-project.git
7. git branch -M main
8. git push -u origin main

Then go to GitHub → Settings → Pages → Branch: main / folder: /docs → Save. Wait a few minutes and visit:
`https://jesshack10.github.io/my-project`

## Quick local steps (gh-pages approach)
1. Create and switch to branch: `git checkout -b gh-pages`
2. Put your site root files at the repository root on this branch (index.html etc.)
3. Commit and push: `git push -u origin gh-pages`
4. In GitHub → Settings → Pages → Branch: gh-pages → Save
