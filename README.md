# With Cathy – website (static export)

A plain HTML/CSS site with no build step and no dependencies. Every page is a self-contained `.html` file; images are in `images/`. Fonts load from Google Fonts (Lexend + Source Serif 4).

## Pages

| File | Page |
|---|---|
| `index.html` | Homepage |
| `terms.html` | Terms & Conditions |
| `termeni.html` | Termeni și Condiții |
| `privacy.html` | Privacy Policy |
| `confidentialitate.html` | Politica de Confidențialitate |
| `delivery-cancel.html` | Delivery, Return & Cancellation Policy |

The current live site uses `/terms`, `/termeni`, `/privacy`, `/confidentialitate` and `/deliver-cancel` (no `.html`). Keep those URLs working when you deploy: either enable "clean URLs" on the host or add redirects (note the live slug is `deliver-cancel`, the file here is `delivery-cancel.html`).

## "Have a quick chat" pop-up

Every "Have a quick chat" button opens a pop-up (vanilla JS at the bottom of each page) with:
- a WhatsApp link (pre-filled message)
- the Google Calendar appointment-scheduling embed

Close: the × button, a click outside, or Esc.

## Still to do before launch

- **Video**: the homepage has a placeholder block marked `[Video – placement to confirm]`. Replace it with the real video (`<video>` for a self-hosted MP4, or a YouTube/Vimeo embed).
- **"Book Make the Call" / "Book Decisive As Fuck"** buttons currently jump to `#book`. Point them at checkout links if those exist.
- Optional: add a favicon, Open Graph image and analytics.

## Deploying with Claude Code

Open this folder in Claude Code and ask, for example:

> Deploy this static site to [Netlify / Vercel / Cloudflare Pages / my host]. Keep the existing URLs /terms, /termeni, /privacy, /confidentialitate and /deliver-cancel working, and point withcathy.com at it.

⚠️ withcathy.com currently runs on GoModern. Switching the domain to a new host replaces the existing site, including any GoModern-hosted products, memberships or checkout pages. Check what else lives on the domain before changing DNS, or deploy to a subdomain first (e.g. `new.withcathy.com`) to test.
