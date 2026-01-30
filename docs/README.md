# TinyToolbox GitHub Pages

This directory contains the GitHub Pages site for TinyToolbox applications, built with Jekyll using the Hacker theme.

## Site Structure

- `_config.yml` - Jekyll configuration
- `_layouts/` - Custom Jekyll layouts
- `index.md` - Main landing page showcasing all apps
- `tinyrecorder.md` - Detailed page for TinyRecorder app
- `privacy.md` - Privacy policy page
- `assets/css/custom.css` - Custom styling on top of Hacker theme
- `CNAME` - Custom domain configuration (for tinytoolbox.app)
- `Gemfile` - Ruby dependencies

## Local Development

To preview the site locally:

1. Install Ruby and Bundler (if not already installed)
2. Install dependencies:
   ```bash
   bundle install
   ```
3. Run Jekyll locally:
   ```bash
   bundle exec jekyll serve
   ```
4. Visit http://localhost:4000

Alternatively, without Jekyll:
```bash
python -m http.server 8000
# Then visit http://localhost:8000 (won't have Jekyll features)
```

## Publishing to GitHub Pages

1. Push the `docs` folder to the main branch
2. Go to repository Settings > Pages
3. Set Source to "Deploy from a branch"
4. Select branch: `main` and folder: `/docs`
5. Save and wait for deployment

## Custom Domain Setup

When you're ready to use the custom domain (tinytoolbox.app):

1. Configure your DNS with your domain registrar:
   - Add an A record pointing to GitHub Pages IPs:
     - 185.199.108.153
     - 185.199.109.153
     - 185.199.110.153
     - 185.199.111.153
   - Or add a CNAME record pointing to: `neeraj9.github.io`

2. In repository Settings > Pages, add custom domain: `tinytoolbox.app`

3. Enable "Enforce HTTPS"

## Adding New Apps

To add a new app to the site:

1. Create a new Markdown file (e.g., `newapp.md`) following the structure of `tinyrecorder.md`
2. Add front matter with title and description
3. Add the app card to `index.md` in the apps section
4. Update navigation in `_layouts/default.html` if needed

## Updating Content

All content is in Markdown files (`.md`) with YAML front matter. The site uses:
- Jekyll static site generator
- Hacker theme (dark, terminal-style design)
- Custom CSS overlay in `assets/css/custom.css`
- Responsive design (mobile-friendly)
- SEO optimization via jekyll-seo-tag

## Notes

- All pages link to privacy policy and GitHub repository
- Microsoft Store links are placeholders (#) - update when apps are published
- Site is optimized for SEO with proper meta tags
- Fully responsive design works on all devices
