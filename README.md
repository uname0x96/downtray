# Downtray website

Static site for [Downtray](https://github.com/uname0x96/downtray), the menu bar inbox for new
downloads on macOS. Three pages, no build step: `index.html`, `support.html`, `privacy.html`.

## Publish on GitHub Pages

1. Push this folder to a public repository (for example `uname0x96/downtray`).
2. Settings → Pages → Source: "Deploy from a branch", branch `main`, folder `/ (root)`.
3. The site is live at `https://uname0x96.github.io/downtray/` within a minute.

## Before going live

- Replace `SUPPORT_EMAIL` in `support.html` and `privacy.html` with the real address.
- Replace `APP_STORE_URL` in `index.html` with the App Store link once the app is approved.
- Swap `images/mac-app-store-badge.svg` for the official badge from
  https://developer.apple.com/app-store/marketing/guidelines/ (Apple asks for its own artwork).

## Custom domain later

Add a `CNAME` file containing the domain (for example `downtray.app`), point the domain's DNS
at GitHub Pages, and update the three URLs in App Store Connect. No other change is needed.

