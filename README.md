# ksaitor.com

A Jekyll site containing Raman Shalupau's essays. Content lives in this repository; there is no web admin.

## Add or edit an essay

1. Add a Markdown file at `_posts/YYYY-MM-DD-short-slug.md`. The date in the filename is the publication date. Use lowercase words separated by hyphens for new slugs.
2. Start with front matter like this:

   ```yaml
   ---
   layout: post
   title: "A descriptive title"
   description: "A concise, accurate summary for search results and sharing."
   image: /images/example.jpg # optional; defaults to the site's social image
   tags: [example] # optional
   ---
   ```

3. Write the article in Markdown. Put images in `images/`, use descriptive alt text, and link to reliable sources where appropriate. The first paragraph is used as the homepage excerpt; keep it useful on its own.
4. Preserve existing filenames, post dates, and permalinks when updating articles. The URL pattern is `/:year-:month-:day/:title/`; changing a filename can break incoming links and search traffic. Do not invent facts, quotes, dates, or claims for SEO.
5. Review the generated post, homepage, archive, feed, sitemap, canonical URL and social metadata before publishing when verification is authorized. A future-dated post may not appear in a normal build.

Use `image` for a post's social image; it may be a site-relative path or an absolute HTTPS URL. Existing image URLs have been preserved. Images and descriptions affect presentation but do not guarantee search rankings.

## Local preview

Install Ruby and Bundler, then run:

```sh
bundle install
bundle exec jekyll serve
```

Open the local URL printed by Jekyll. `Gemfile.lock` pins the local dependency set; update it deliberately when changing dependencies. This local setup uses Jekyll 4, so it is not an exact reproduction of the hosted build.

## Publishing

GitHub Pages is configured to build the root of the `master` branch at `ksaitor.com`. An authorized push to that branch can publish changes; do not push or change deployment settings without explicit authorization. Check the GitHub Pages deployment and live pages after publishing.

The current GitHub Pages branch builder uses its own supported Jekyll and plugin versions, not this repository's lockfile. For fully reproducible production builds, migrate to a GitHub Actions Pages workflow and change the repository's Pages source to GitHub Actions; that migration requires a deployment configuration change and live verification. Keep `CNAME` and existing permalinks during any migration.

## Integrations

- `jekyll-seo-tag` generates canonical, Open Graph, Twitter and structured metadata; set post `description` and `image` in front matter.
- Sitemap and RSS are generated at `/sitemap.xml` and `/feed.xml`.
- Disqus comments and the Substack subscription embed are retained. Existing embedded tweets use the Twitter widget.
- Google Analytics is disabled until a real GA4 measurement ID is set under `google-analytics.id` in `_config.yml`.
