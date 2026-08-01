DNS setup for gentle-giant.dev
=============================

Follow these steps at your domain registrar to make `gentle-giant.dev` (apex) and `www.gentle-giant.dev` point to your GitHub Pages site.

1) Apex domain (gentle-giant.dev)
  - Add four A records pointing to GitHub Pages IPs:
    - 185.199.108.153
    - 185.199.109.153
    - 185.199.110.153
    - 185.199.111.153

2) www subdomain (www.gentle-giant.dev) — recommended
  - Add a CNAME record for `www` pointing to `spearKNIGHTakis.github.io` (no trailing slash).

3) Verify and enable HTTPS
  - In your repository Settings → Pages, ensure the custom domain is set to `gentle-giant.dev`.
  - Enable "Enforce HTTPS" once GitHub issues the TLS certificate (may take a few minutes to an hour).

4) If you prefer the `github.io` URL instead
  - Remove the `CNAME` file from the repository and push; Pages will serve at:
    `https://spearKNIGHTakis.github.io/gentle_giant_dev/`

Notes
  - DNS changes can take up to 48 hours, but usually propagate within minutes to a few hours.
  - If your registrar supports ALIAS/ANAME records for apex domains you can use those instead of multiple A records.

Example registrar steps (Cloudflare, Namecheap, GoDaddy will each have a DNS panel — create the above records there).
