# HiTrek public site (GitHub Pages)

Small **public** static site for App Store privacy URL and a tiny landing page.
The HiTrek app repo stays private — this repo only contains HTML/CSS.

## App Store URL

```
https://pszakal.github.io/hitrek-site/privacy/
```

Use relative asset links (not `/styles.css`) so GitHub project Pages under `/hitrek-site/` works.


## Deploy (GitHub Pages)

```bash
cd hitrek-site
git init
git add .
git commit -m "Add HiTrek privacy policy site for App Store"
gh auth refresh -h github.com   # if gh token is expired
gh repo create hitrek-site --public --source=. --remote=origin --push
```

Then on GitHub: **Settings → Pages → Build from branch `main` / root**.

Free Pages requires a **public** repo. That is expected for a privacy policy; it does not expose the HiTrek app source.

## Local preview

```bash
npx --yes serve .
# open http://localhost:3000/privacy/
```
