# PawGearVerified Homepage

Open `elementor-homepage.html` in a browser for a standalone preview, or paste its entire contents into an Elementor **HTML** widget or a WordPress **Custom HTML** block.

## Cloudflare deployment

The files inside `public/` are the deployed website. Cloudflare Workers Builds should use:

- Install command: `npm install`
- Deploy command: `npx wrangler deploy`
- Production branch: `main`

The Worker name and static-assets directory are configured in `wrangler.jsonc`. Once the repository is connected to Cloudflare, a commit to `main` deploys the updated site to `https://pawgearverified-site.2498378660.workers.dev/`.

## Before publishing

1. Upload `assets/pawgearverified-logo-web.png` to the WordPress Media Library, then replace both `src="assets/pawgearverified-logo-web.png"` paths with the Media Library URL. A full-resolution transparent version is available at `assets/pawgearverified-logo.png`, and the original supplied file is preserved at `assets/pawgearverified-logo-source.jpg`.
2. Use `assets/pawgearverified-mark.png` as the site icon or favicon in WordPress.
3. Replace the Unsplash image URLs with original photos uploaded to the WordPress Media Library. Keep the descriptive `alt` text and the existing image dimensions to avoid layout shift.
4. Create the linked WordPress pages/slugs: `/about/`, `/affiliate-disclosure/`, `/privacy-policy/`, `/reviews/`, and the category archive or taxonomy URLs.
5. Replace the three placeholder review links with real WordPress article URLs.
6. Add affiliate destination links only inside review articles or additional card CTAs. Use `rel="sponsored nofollow noopener"` on external affiliate links and keep a clear FTC disclosure before the first affiliate link.
7. Keep new categories limited to grooming brushes, litter mats, tough chew toys, outdoor water bottles, car safety accessories, cat scratching boards, and fence accessories.
8. Replace the footer year with the site's WordPress-generated year if the theme does not already provide dynamic footer content.

The layout uses no JavaScript. All CSS selectors are scoped to `.pgv-site`, so it can be embedded without affecting Elementor's surrounding sections.
