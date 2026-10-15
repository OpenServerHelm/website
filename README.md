# OpenServerHelm website

Source for the standalone public information site for **openserverhelm.com**.

**Status:** initial static website candidate, pending owner review and publication. This is *not* the management dashboard or an installation package.

## Structure

- `index.html` — static accessible home page; scoped, system-aware light/dark appearance and responsive navigation
- `.nojekyll` — use static files directly when hosted via GitHub Pages

## Publishing approach

The website will use its **own GitHub repository**, independent of both the private development code and public product source. The source is self-contained: no third-party fonts, analytics, images, embedded authentication or external services.

**Recommended GitHub Pages setup after approval:**
1. Audit and approve the source, then set only the *website* repository public.
2. In website repository Settings → Pages, select **Deploy from a branch**, choose `main` and root `/`.
3. Verify the temporary GitHub Pages URL and site content over HTTPS.
4. Set **Custom domain** to `openserverhelm.com` in Pages and verify required DNS guidance.
5. In Cloudflare, create apex A/AAAA records pointing to GitHub Pages' published addresses (do not proxy until HTTPS verified), then configure `www` alias if desired. Confirm GitHub Pages certificate issuance and enforce HTTPS.
6. Recheck domain ownership, redirects, TLS, security headers/limits, and mobile appearance. Keep rollbacks as previous Git commits.

Do not apply speculative DNS addresses or claim that hosting is live until GitHub's Pages status and an independent HTTPS fetch verify it. Changing Cloudflare records is performed with owner approval, separate from the private app or VPN.

The launch page describes **planned** product capabilities. It must not advertise releases, downloads, enterprise certification, community forums, source URLs or verified OS support until available.

## Security

This site has no backend, forms, identity integration or analytics, and contains no infrastructure endpoints. Do not add privately hosted images, true server addresses, owner identities, tokens or AI development context. No platform login is linked from the public site.

Content and design should remain accessible on desktop/mobile and must not borrow Star Trek licensed artwork or Kubernetes Helm marks.
