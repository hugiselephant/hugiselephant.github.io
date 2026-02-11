# Task List for hugiselephant.github.io

A prioritized list of improvements and maintenance tasks for the personal blog.

---

## High Priority

### 1. Update GitHub Actions Workflow
- [ ] Upgrade `actions/checkout` from `v2` to `v4`
- [ ] Upgrade `peaceiris/actions-hugo` from `v2` to latest
- [ ] Upgrade `peaceiris/actions-gh-pages` from `v3` to latest
- [ ] Upgrade runner from `ubuntu-20.04` (EOL) to `ubuntu-latest`
- [ ] Pin Hugo to a specific version instead of `latest` for reproducible builds

### 2. Fix Content Typos and Filenames
- [ ] Rename `Rubber band of knwledge.md` → `Rubber band of knowledge.md` (typo in filename)
- [ ] Rename `Spacial Computing.md` → `Spatial Computing.md` (typo in filename)
- [ ] Audit all pages for spelling/grammar issues

### 3. Improve Content Metadata Consistency
- [ ] Ensure all pages have `date` and `lastmod` fields in frontmatter
- [ ] Add `description` fields to pages that are missing them (helps SEO and social sharing)
- [ ] Standardize `tags` and `categories` usage across all pages

---

## Medium Priority

### 4. Fix RSS Feed URL
- [ ] Update RSS `url` in `config.yml` from `https://hugiselephant.github.io/index.xml` to `https://hugiselephant.com/index.xml` (should match the custom domain)

### 5. Complete or Remove the Contact Form
- [ ] The `contact.html` shortcode has a form with `action="#"` — either integrate a form backend (e.g., Formspree, Netlify Forms) or remove the unused shortcode

### 6. Add Image Optimization
- [ ] Consider adding Hugo's built-in image processing for responsive images
- [ ] Add `loading="lazy"` to image templates for better page performance
- [ ] Evaluate compressing existing images in `content/assets/` (~16 MB total)

### 7. Improve the Home Page and Site Identity
- [ ] Add a profile photo or avatar to the home page
- [ ] Consider adding a brief "About" page with more context about the author
- [ ] Update or customize the site's favicon

---

## Low Priority

### 8. Enhance the Backlinks Partial
- [ ] Format `backlinks.html` for readability (currently compressed into few lines)
- [ ] Add styling or a count indicator (e.g., "3 notes link to this note")
- [ ] Consider adding bidirectional link previews on hover

### 9. Add a 404 Page
- [ ] Create a custom `layouts/404.html` with a friendly message and navigation back to the home page

### 10. Improve Search UX
- [ ] Verify search works correctly with all 43 pages
- [ ] Consider adding search result previews or excerpts

### 11. Add Sitemap and Robots.txt Configuration
- [ ] Hugo generates these by default, but verify they are correctly configured for the custom domain
- [ ] Add a `robots.txt` template if custom rules are needed

### 12. Theme Maintenance
- [ ] Check if PaperMod theme has upstream updates worth pulling in
- [ ] Review theme overrides to ensure they still work with the latest theme version

---

## Content Ideas (Ongoing)
- [ ] Continue regular posting cadence (~1-2 posts per month)
- [ ] Consider creating a "Best Of" or "Start Here" page to guide new readers
- [ ] Add interlinks between related posts to strengthen the knowledge graph
