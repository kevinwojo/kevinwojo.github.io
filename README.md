# kevinwojo.github.io

Tech blog built with [Hugo](https://gohugo.io/) and the
[Paper](https://github.com/nanxiaobei/hugo-paper) theme.

## Local development

Requires Hugo (extended) and Go — Go is what fetches the theme, which is wired
up as a Hugo Module rather than a vendored `themes/` directory.

```sh
hugo mod get github.com/nanxiaobei/hugo-paper   # first checkout only; pins the theme in go.mod
hugo server -D                                   # http://localhost:1313
```

## Writing

```sh
hugo new posts/my-post.md
```

Posts start as `draft: true`; flip it to `false` (or delete the line) to publish.

## Deploying

Pushing to `main` runs `.github/workflows/hugo.yml`, which builds the site and
publishes it to GitHub Pages. This requires **Settings → Pages → Source** to be
set to **GitHub Actions**.
