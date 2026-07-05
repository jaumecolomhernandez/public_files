# Hosting the Privacy Policy & Terms of Service

This folder contains two ready-to-host static pages:

- `privacy.html` — Privacy Policy
- `terms.html` — Terms of Service

Enable Banking requires **public HTTPS URLs** for the Privacy URL and Terms URL
when you register a **production** application in the Control Panel. Both pages
below are self-contained (inline CSS, no build step, no external assets), so you
can host them anywhere that serves static files.

> **These pages are templates, not legal advice.** Review them and make sure they
> accurately describe your app before publishing.

---

## ⚠️ Before you publish (required)

1. Open both `privacy.html` and `terms.html`.
2. Replace every `your-email@example.com` placeholder with a **real** contact email.
3. In `terms.html`, confirm the governing law (`Spain`) is correct for you.
4. Skim each page to confirm it matches how your app actually works.

---

## Option A — GitHub Pages (fastest reliable option)

GitHub Pages gives you stable `https://` URLs for free.

1. **Create a GitHub account** (if you don't have one) at <https://github.com>.
2. **Create a new public repository**, e.g. named `finance-legal`.
   - On the repo creation page, keep it **Public** (Pages needs Public on free accounts).
3. **Upload the two files**:
   - Click **Add file → Upload files**.
   - Drag `privacy.html` and `terms.html` into the page.
   - Click **Commit changes**.
4. **Enable Pages**:
   - Go to the repo's **Settings → Pages**.
   - Under **Build and deployment → Source**, choose **Deploy from a branch**.
   - Set **Branch** to `main` and folder to `/ (root)`, then **Save**.
5. **Wait ~1 minute**, then refresh the Settings → Pages screen. It will show:
   `Your site is live at https://<your-username>.github.io/finance-legal/`
6. Your two URLs are:
   - Privacy: `https://<your-username>.github.io/finance-legal/privacy.html`
   - Terms:   `https://<your-username>.github.io/finance-legal/terms.html`

Open both URLs in a browser to confirm they load over `https://`.

---

## Option B — GitHub Gist (quick alternative)

Good if you want the fastest possible route without creating a repo. Uses the
free <https://raw.githack.com> CDN so the HTML renders as a page (a raw Gist URL
serves as plain text, which Enable Banking may reject).

1. Go to <https://gist.github.com> (signed in).
2. Create a **public** gist. Add two files named exactly `privacy.html` and
   `terms.html`, pasting the contents of each. Click **Create public gist**.
3. On each file, click the **Raw** button and copy the URL. It looks like:
   `https://gist.githubusercontent.com/<user>/<gistid>/raw/<hash>/privacy.html`
4. Convert each raw URL to a rendered one with **raw.githack.com**: replace
   `https://gist.githubusercontent.com/` with `https://gist.githack.com/`.
   Example result:
   `https://gist.githack.com/<user>/<gistid>/raw/<hash>/privacy.html`
5. Use those `githack` URLs as your Privacy and Terms URLs.

> Tip: GitHub Pages (Option A) gives cleaner, more stable URLs and is recommended
> for a production registration.

---

## What to paste into Enable Banking

In the Enable Banking **Control Panel → your production application settings**,
fill in:

- **Privacy URL:** `https://<your-username>.github.io/finance-legal/privacy.html`
- **Terms URL:** `https://<your-username>.github.io/finance-legal/terms.html`

(Or the equivalent `gist.githack.com` URLs if you used Option B.)

Both must start with `https://` and load publicly in an incognito/private
browser window. Test them there before submitting.
