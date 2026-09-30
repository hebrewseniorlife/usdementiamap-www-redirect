# www.usdementiamap.org redirect

Sends `www.usdementiamap.org` to `https://usdementiamap.org`, where the
[US Dementia Map](https://usdementiamap.org/) runs on Posit Connect Cloud.

Connect Cloud allows one custom domain per app, and the app uses the bare domain.
This repo is served by GitHub Pages at the `www` name instead, and GitHub issues its
HTTPS certificate.

- `index.html` redirects, keeping the path, query string and fragment.
- `404.html` is the same page, so any path under `www` redirects too.
- `CNAME` tells GitHub Pages which domain this site answers for.

DNS (at whois.com): `www` is a CNAME to `hebrewseniorlife.github.io`. The bare domain
is a CNAME to `edge.connect.posit.cloud` and is not affected by this repo.
