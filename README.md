# siglattice.com

Public GitHub Pages site for `siglattice.com` and its OAuth-facing policy pages.

## Files

- `index.html`: application home page
- `privacy-policy/index.html`: privacy and Google user-data disclosure
- `terms-of-service/index.html`: terms of service
- `assets/site.css`: shared responsive presentation
- `assets/siglattice-mark.svg`: original grid mark and favicon
- `assets/siglattice-mark-512.png`: square raster mark for app branding and touch icons
- `assets/siglattice-mark-120.png`: exact-size Google OAuth consent-screen logo
- `CNAME`: custom domain for GitHub Pages
- `.nojekyll`: disables Jekyll processing so root files are served as-is

## GitHub Pages

Enable GitHub Pages for this repository and set the source to the `main` branch root. With the included `CNAME` file, GitHub Pages will provision the site for `siglattice.com`.

## Personal introduction

The homepage is a hand-authored, dependency-free introduction to an ongoing
life experiment. `assets/primer.css` styles it; it uses the original
`assets/siglattice-mark.svg`. Policy pages retain `assets/site.css`.

The page distinguishes domains as a naming idea from SigLattice as the
development ecosystem using them. It contains no demonstration records, private
data connection, tracking script, or example domain inventory.

Preview with a local static server. Review phone, tablet, and desktop layouts,
then verify profile/contact/policy links before publishing. Production still
publishes the root of `main`.
