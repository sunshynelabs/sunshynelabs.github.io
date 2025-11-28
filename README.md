# Sunshyne Labs — GitHub Pages

This repository is served via GitHub Pages (branch `main`, root). Key deployment notes:

- The custom domain is `sunshynelabs.com`. Ensure DNS is configured correctly (see below).
- Pages source: `main` branch, `/ (root)`.
- Use Jekyll pages (the site contains Markdown pages and some static HTML assets).

DNS / GitHub Pages checklist

1. For apex domain (`sunshynelabs.com`) add A records pointing to GitHub Pages:

   - 185.199.108.153
   - 185.199.109.153
   - 185.199.110.153
   - 185.199.111.153

   OR use `www` as a CNAME to `sunshynelabs.github.io` and make `www` canonical.

2. In GitHub → Settings → Pages, enter `sunshynelabs.com` as the custom domain and enable HTTPS. Wait for certificate provisioning.

3. After DNS and Pages are configured, verify URLs:

   ```bash
   dig +short A sunshynelabs.com
   curl -I -L https://sunshynelabs.com
   curl -I -L https://sunshynelabs.github.io/example-corp/
   ```

Repository maintenance notes

- Keep a single canonical source for pages — avoid nested duplicate folders like `example-corp/example-corp`.
- If you prefer the Jekyll-generated homepage, remove `index.html` (static) — done in this PR. If you want the static page instead, revert.
- Contact: `hello@sunshynelabs.com` is used as canonical contact in `404.html` and `contact.md`.

If you'd like, I can now commit & push these changes to `main` from this environment, or provide the exact `git` commands for you to run locally.
# sunshynelabs.github.io
Building better tomorrows. Sunshyne Labs. With AI. For humans.
