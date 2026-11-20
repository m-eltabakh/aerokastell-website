# aerokastell-website

The AeroKastell one-page stealth landing — a static site hosted on
**GitHub Pages** at **https://aerokastell.com** (custom domain).

One page only: the brand, the slogan and a quiet animated backdrop while we
build in stealth mode. Everything here comes from the official brand repo
(`aerokastell-branding`) — never redraw the logo; update assets by re-copying
the current exports.

## Files

| File | What it is |
|---|---|
| `index.html` | The whole site (one page, inline CSS, no JavaScript) |
| `CNAME` | GitHub Pages custom domain: `aerokastell.com` |
| `assets/ak-logo-horizontal-reversed-v4.svg` | Official reversed lockup (from `aerokastell-branding/brand/logo/svg/`) |
| `assets/favicon.ico`, `ak-favicon.svg`, `ak-apple-touch-icon-180.png` | Official icons (from `brand/icons/`) |
| `assets/hero/ak-hero-loop-v01.*` | The seamless 10 s website backdrop (from `out/motion/hero/`; poster shown for reduced motion) |
| `assets/fonts/lato-*.woff2` | Self-hosted Lato 400/700/900 (open licence, OFL) |

## Deploy (GitHub Pages)

1. Push `main` to GitHub.
2. Repo **Settings → Pages** → Source: *Deploy from a branch* → `main` / `/(root)` → Save.
3. **Settings → Pages → Custom domain**: `aerokastell.com` (the `CNAME` file is already in
   the repo). Wait for the DNS check, then tick **Enforce HTTPS**.

## DNS (Namecheap)

**aerokastell.com → Advanced DNS:**

| Type | Host | Value |
|---|---|---|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| CNAME | www | `<github-username>.github.io` |

**aerokastell.ai:** set up domain forwarding → `https://aerokastell.com` (GitHub Pages
serves one custom domain per site; the second domain redirects).

**Email:** set up Namecheap's free email forwarding (`hello@aerokastell.com` → your inbox)
so the page's mailto link works.

## Notes and placeholders

- The slogan "Evidence, not just alarms." is a **draft tagline** from the brand context
  (`aerokastell-branding/docs/brand-context.md`) — change it there when it's approved.
- The contact email only works once email forwarding is configured.
- No `og:image` yet: the current brand link-preview image has the placeholder domain
  (`aerokastell.de`) baked in. Rebuild the social assets with the real domain first
  (`scripts/build_social.py` in the brand repo), then add `og:image`.
- Colours/type follow the brand: Kastell Night `#0B1F33`, Signal Red `#E0383E`,
  Steel Light `#7D8D9C` on dark, Lato throughout.
