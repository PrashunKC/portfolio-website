# Deployment guide

This repository is a single static site. The entry point is [`index.html`](index.html);
CSS and JavaScript are embedded in that file. There is no build step, package
manager, server-side application, or form backend in this repository.

## Test locally

From the repository directory, use any static HTTP server:

```bash
python3 -m http.server 8000
```

Open <http://localhost:8000>. Serving over HTTP is preferable to opening the
file directly because it matches a hosted deployment and avoids browser
restrictions around local resources.

Before publishing, check the navigation anchors, project links, theme toggle,
typing/particle effects, responsive layout, and external font/icon resources.
The contact form is presentation-only in the current HTML; it does not submit
to a backend.

## GitHub Pages

1. Push the repository to GitHub.
2. Open **Settings → Pages**.
3. Select the deployment branch and the repository root (`/`) as the source.
4. Save and wait for the Pages deployment.
5. Keep [`CNAME`](CNAME) at the repository root if using the configured custom
   domain.

GitHub Pages serves `index.html` automatically. Do not rename it to the old
`prashunkc-portfolio.html` filename referenced by earlier versions of this
guide.

## Other static hosts

Netlify, Vercel, traditional shared hosting, and object-storage website
hosting can all deploy this directory without a build command. Set the
publish directory to the repository root and use `index.html` as the entry
document. Configure the custom domain and DNS records in the host's current
dashboard; record names and IP addresses vary by provider and should not be
copied from an old guide.

## Custom domain checklist

- Confirm the host has issued an HTTPS certificate.
- Configure the apex and/or `www` DNS records exactly as the host requests.
- Keep `CNAME` aligned with the hostname configured in the hosting provider.
- Allow time for DNS propagation and verify both HTTP and HTTPS redirects.

## Maintenance

Update the content in `index.html` directly, then test locally before pushing.
External Google Fonts and Font Awesome CDN links are runtime dependencies; if
offline or self-contained hosting is required, vendor those assets and update
the corresponding `<link>` tags.
