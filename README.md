# What Now site

Three static pages for the What Now iPhone app: a landing page, a support page,
and the privacy policy. No build step, no dependencies: plain HTML with one
shared stylesheet, light and dark, in the app's Paper colors. English only, like
the app.

They exist for two App Store requirements:

- **Guideline 5.1.1(i)**: a privacy policy link reachable inside the app.
- **Guideline 1.5**: a Support URL in App Store Connect, which must be a web
  page (a `mailto:` address isn't accepted in that field).

Published with GitHub Pages from `emadrahman/whatnow-site`, branch `main`,
folder `/ (root)`.

## URLs

| Page | URL | Where it goes |
|---|---|---|
| Landing | `https://emadrahman.github.io/whatnow-site/` | App Store Connect *Marketing URL* (optional) |
| Support | `https://emadrahman.github.io/whatnow-site/support.html` | App Store Connect *Support URL* |
| Privacy policy | `https://emadrahman.github.io/whatnow-site/privacy.html` | `AboutLinks.privacyPolicy` in the app's `AboutView.swift`, and the App Store Connect *Privacy Policy URL* |

The privacy policy URL is compiled into the app, so moving it means shipping a
new build. If a custom domain is likely, point it at this repository first.

## Maintenance

Update the "Last updated" date at the top of `privacy.html` whenever its
substance changes, and note material changes in the app's What's New. The
policy describes what the app actually does with calendar data, so revisit it
whenever the app starts reading, storing, or sending anything new (a server for
wake-up pushes, iCloud sync, analytics).
