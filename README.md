# Tech Notes Blog

My blog about IT support and networking, built with **Jekyll** and hosted free on
**GitHub Pages**. GitHub builds the site automatically: you just write Markdown.

**Live blog:** https://bongokuhle-nokubonga.github.io/tech-blog/

## Write a new post

1. Add a file to `_posts/` named `YYYY-MM-DD-short-title.md`, for example `2026-12-01-active-directory-basics.md`
2. Start it with this header:

   ```markdown
   ---
   layout: post
   title: "Your Post Title"
   tags: [networking, windows]
   ---
   ```

3. Write the post in Markdown below the header
4. Commit and push. The blog updates in about a minute

You can do all of this in the browser on GitHub: open `_posts`, then **Add file → Create new file**.

## Deploy to GitHub Pages

1. Push this folder to a GitHub repository called `tech-blog`
2. In `_config.yml`, set `linkedin_url` to your LinkedIn profile
3. On GitHub, open **Settings → Pages**, choose **Deploy from a branch**, branch `main`, folder `/ (root)`, then click **Save**

## Structure

```
_config.yml        site title, links and settings
_layouts/          page templates (default + post)
_posts/            blog posts in Markdown
assets/css/        styles (with automatic dark mode)
about.md           About page
index.html         list of posts
```
