# YZ International Business

Commercial site for YZ International Business, staged for GitHub Pages at **ib.yurizanoni.com**.

This is the preserved and slightly improved one-pager previously published at [yurizanoni.com](https://yurizanoni.com). The apex domain will become Yuri Zanoni’s personal site after cutover. Do not point this repository at the apex. Live apex was left untouched (`studiozanoni/yurizanoni.com` `main` remains the current IB site).

Contact: [yurizanoni@gmail.com](mailto:yurizanoni@gmail.com) · WhatsApp [+852 5262 4903](https://wa.me/85252624903)

## GitHub Pages — human / UI step still required

The deploy workflow is in `.github/workflows/pages.yml`, but the first runs failed with:

`Create Pages site failed. Error: Resource not accessible by integration`

A `GITHUB_TOKEN` cannot enable Pages on a new repository. Enable it once in the GitHub UI, then the custom domain can be attached.

1. Open [Settings → Pages](https://github.com/studiozanoni/ib.yurizanoni.com/settings/pages).
2. Preferred, matching the live apex setup: **Deploy from a branch** → `main` / `/ (root)` → Save.
   Alternative: set source to **GitHub Actions**, then re-run the “Deploy GitHub Pages” workflow.
3. Custom domain: `ib.yurizanoni.com`. After DNS is green, enable **Enforce HTTPS**.

Until that is done, the project URL `https://studiozanoni.github.io/ib.yurizanoni.com/` will 404.

Temporary source preview (CSS-relative, usable now):

- https://raw.githack.com/studiozanoni/ib.yurizanoni.com/main/index.html

## DNS (Cloudflare)

Leave apex `A`/`AAAA` and `www` untouched until the personal site is ready to ship **and** this subdomain is live.

Add only:

| Type | Name | Target | Proxy |
| --- | --- | --- | --- |
| CNAME | `ib` | `studiozanoni.github.io` | **DNS only** (proxy off) |

Do not change MX, SPF, or DKIM. Email forwards (`yuri@`, `fluxoyz@`, `contato@`, `contact@` → `yurizanoni@gmail.com`) must stay.

## Cutover note

After `ib.yurizanoni.com` is serving this site on HTTPS, the personal monument can replace the apex. Then add a discreet link from this site back to `https://yurizanoni.com/` if desired. Do not add that link while the apex is still this one-pager.
