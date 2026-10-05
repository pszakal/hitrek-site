# HiTrek public site (GitHub Pages)

Small **public** static site for App Store privacy URL and a tiny landing page.
The HiTrek app repo stays private — this repo only contains HTML/CSS.

## App Store URL

After Pages is live, use:

```text
https://<github-user>.github.io/hitrek-site/privacy/
```

Or, if you use a custom domain / user site (`username.github.io`):

```text
https://hitreklabs.com/privacy/
```

## Before you publish

1. Replace contact details if needed (search for `privacy@hitreklabs.com` and `HiTrek Labs` in `privacy/index.html`).
2. Confirm Mixpanel residency (site text assumes EU endpoint — matches `hi-trek` analytics defaults).

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
