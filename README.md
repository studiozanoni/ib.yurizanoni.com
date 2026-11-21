# YZ International Business

Commercial site for YZ International Business, staged for GitHub Pages at **ib.yurizanoni.com**.

This is the preserved and slightly improved one-pager previously published at [yurizanoni.com](https://yurizanoni.com). The apex domain will become Yuri Zanoni’s personal site after cutover. Do not point this repository at the apex.

Contact: [yurizanoni@gmail.com](mailto:yurizanoni@gmail.com) · WhatsApp [+852 5262 4903](https://wa.me/85252624903)

## GitHub Pages

- Source: `main`, site root (`/`), deployed with `.github/workflows/pages.yml`.
- Custom domain file: `CNAME` → `ib.yurizanoni.com`.
- Preview (until the custom domain is attached): `https://studiozanoni.github.io/ib.yurizanoni.com/`

If Pages is not yet enabled after the first push:

1. GitHub → this repository → **Settings** → **Pages**.
2. Source: **GitHub Actions** (preferred), or **Deploy from a branch** → `main` / `/ (root)`.
3. Custom domain: `ib.yurizanoni.com`. Wait for DNS, then enable **Enforce HTTPS**.

A `GITHUB_TOKEN` 403 on the Pages API is expected in some setups; use the UI steps above.

## DNS (Cloudflare)

Leave apex `A`/`AAAA` and `www` untouched until the personal site is ready to ship **and** this subdomain is live.

Add only:

| Type | Name | Target | Proxy |
| --- | --- | --- | --- |
| CNAME | `ib` | `studiozanoni.github.io` | **DNS only** (proxy off) |

Do not change MX, SPF, or DKIM. Email forwards (`yuri@`, `fluxoyz@`, `contato@`, `contact@` → `yurizanoni@gmail.com`) must stay.

## Cutover note

After `ib.yurizanoni.com` is serving this site on HTTPS, the personal monument in `studiozanoni/yurizanoni.com` can be merged to `main`. Then add a discreet link from this site back to `https://yurizanoni.com/` if desired. Do not add that link while the apex is still this one-pager.
