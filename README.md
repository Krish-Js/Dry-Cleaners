# Valley Cleaners Website

Simple static website for **Valley Cleaners** in Chesterfield, Missouri.

## Local preview

```bash
python -m http.server 4173
```

Open: <http://localhost:4173>

## Deployable domain setup (GitHub Pages)

This repository includes:

- `.github/workflows/deploy.yml` to deploy the site to GitHub Pages on every push to `main`.
- `CNAME` configured for: `valleycleanerschesterfield.com`.

### 1) Enable GitHub Pages

In your GitHub repository:

1. Go to **Settings → Pages**.
2. Under **Build and deployment**, set **Source** to **GitHub Actions**.

### 2) Configure DNS at your domain registrar

For root domain (`valleycleanerschesterfield.com`), add **A records**:

- `185.199.108.153`
- `185.199.109.153`
- `185.199.110.153`
- `185.199.111.153`

For `www`, add **CNAME**:

- Host: `www`
- Value: `<your-github-username>.github.io`

### 3) Set domain in GitHub Pages

In **Settings → Pages → Custom domain**, enter:

- `valleycleanerschesterfield.com`

Then check **Enforce HTTPS** once the certificate is ready.

### Notes

- DNS propagation can take a few minutes to 48 hours.
- If you want `www` to be primary instead, set `www.valleycleanerschesterfield.com` as custom domain and adjust DNS/CNAME accordingly.
