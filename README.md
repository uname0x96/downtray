# Downtray website

Static site for [Downtray](https://github.com/uname0x96/downtray-macos), the menu bar inbox for new
downloads on macOS. Three pages, no build step: `index.html`, `support.html`, `privacy.html`.

## Publish on GitHub Pages

1. Push this folder to a public repository (for example `uname0x96/downtray`).
2. Settings → Pages → Source: "Deploy from a branch", branch `main`, folder `/ (root)`.
3. The site is live at `https://uname0x96.github.io/downtray/` within a minute.

## Before going live

- Replace `SUPPORT_EMAIL` in `support.html` and `privacy.html` with the real address.
- The Download buttons point at the Mac App Store listing: https://apps.apple.com/us/app/downtray/id6815153471
- Swap `images/mac-app-store-badge.svg` for the official badge from
  https://developer.apple.com/app-store/marketing/guidelines/ (Apple asks for its own artwork).

## Custom domain later

Add a `CNAME` file containing the domain (for example `downtray.app`), point the domain's DNS
at GitHub Pages, and update the three URLs in App Store Connect. No other change is needed.


## Screenshots and demo video

Everything under `images/popover-*.jpg`, `images/settings-folders.jpg`, `images/demo-poster.jpg`
and `videos/demo.mp4` is a real capture of the Debug build on a Mac, not a mockup. The Debug build
exposes a local bridge (see `docs/architecture.md` in the app repo) that opens the popover and
drives filters, search, trash and rules, while `screencapture -R x,y,w,h` grabs the region under
the menu bar and `screencapture -v -R ...` records the loop. Seed `~/Downloads` with a few sample
files first, put a plain wallpaper behind the popover, and keep the video under a few MB
(`ffmpeg -crf 26 -movflags +faststart`). GitHub Pages serves the MP4 as a normal static file.
