# Junzhe JIN — personal academic website

A self-contained static website: nine HTML pages share `style.css`. There is no
package installation, JavaScript runtime, or application build step. Images and
`CV.pdf` are served directly from the repository root.

## Preview locally

Run `python3 -m http.server 8000` from this directory, then open
http://localhost:8000. Check the home page, publication anchor, research listing,
six project detail pages and photography page on desktop and mobile.

## GitHub Pages deployment

The existing repository uses GitHub's built-in **pages build and deployment**
workflow on `main` (the last inspected successful run was 42031137646). No custom
Actions workflow or framework configuration is needed for this redesign.

1. Review and merge the redesign pull request into `main`.
2. Keep Settings → Pages configured to deploy from `main`, `/ (root)`.
3. Wait for **pages build and deployment** to succeed under Actions.
4. Visit https://junzhe-jin.github.io/ and refresh cached styles if necessary.

No domain, asset paths, or deployment workflow changes are required.

## Visual system and accessibility

`style.css` defines cream paper (#f7f4ed), dark brown text (#332d28), muted brown
(#6e6258), and terracotta links/buttons (#a4492e). The system serif stack uses
Charter, Iowan Old Style, Palatino or Georgia without external font downloads.
It includes responsive navigation, a single-column mobile project grid, visible
keyboard focus, skip-to-content links, reduced-motion support and underlined
inline links. Original research content, destinations and assets are retained;
the home page also exposes the existing CV PDF.

Validation: Chromium/Playwright checked all nine pages at 1440, 390 and 320px,
with no horizontal overflow or broken images. All original link destinations were
retained and local targets checked. Main text, muted text, links and primary
button text exceed WCAG AA 4.5:1 contrast. Desktop and mobile screenshots were
reviewed. Since the site has no application build, the checks used the actual
HTML/CSS served over HTTP; the production Pages build runs after merging.
