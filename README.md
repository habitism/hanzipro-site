# HanziPro website

The official landing page for the iOS and Android versions of HanziPro.

## Local preview

```sh
bundle install
bundle exec jekyll serve
```

Then open `http://127.0.0.1:4000`.

The production site is configured for `https://hanzipro.cn` and can be published with GitHub Pages from the repository's `main` branch.

## SEO

Each page should define a unique `title` and `description` in its front matter.
The shared head generates canonical URLs, Open Graph and Twitter metadata.
The homepage includes MobileApplication JSON-LD using confirmed app information;
pricing and ratings are omitted until verified and displayed on the page. This
basic markup does not meet all Google software-app rich result requirements.

`sitemap.xml` automatically includes pages using the `default` or `page` layout.
Set `sitemap: false` to omit a page from the sitemap (this does not prevent indexing).
`robots.txt` allows crawling and points to the sitemap. Keep `url` in `_config.yml`
set to the production HTTPS domain.

After deployment, verify the domain in Google Search Console and submit
`https://hanzipro.cn/sitemap.xml`. Check indexing with URL Inspection. These
account-level steps are separate from the repository configuration.
