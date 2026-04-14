# Icon Setup

Replace the placeholder files in this folder with real image assets before production launch.

Required files:

- `icon-192.png` - recommended size `192x192`
- `icon-512.png` - recommended size `512x512`
- `apple-touch-icon.png` - recommended size `180x180`

Also replace these related branding files outside this folder:

- `assets/images/logo.png`
- `assets/images/social-share.jpg`
- `favicon.ico`

Current site references:

- Web manifest: `assets/site.webmanifest`
- Favicon: `_layouts/default.html`
- Site logo: `_config.yml`
- Default social image: `_config.yml`

Recommended formats:

- PNG for app icons and logo
- ICO for `favicon.ico`
- JPG or PNG for social share image

Recommended social share image size:

- `1200x630`

After replacing files, rebuild the site:

```bash
bundle exec jekyll build
```
