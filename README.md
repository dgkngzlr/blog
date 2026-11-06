# blog

Source of https://dogukangozler.com. Markdown + [Hugo](https://gohugo.io/) (0.169.0, standard edition)
with the [rewired](https://github.com/RigleGit/rewired) theme, pinned as a git submodule.

The server pulls this repo every 5 minutes and rebuilds the site. Nothing is pushed to the server.
A failed build leaves the live site unchanged.

## Writing

```bash
hugo new content posts/my-post.md   # then edit, set draft: false
hugo server                          # preview at http://localhost:1313
git push                             # live within ~5 minutes
```

- CV PDF: put it at `static/cv.pdf` (linked from `/cv/`).
- No third-party requests (privacy): fonts and icons are self-hosted under `static/vendor/`,
  and `layouts/_partials/head.html` and `head/math.html` override the theme's CDN links.
  Don't add embeds, analytics or CDN links.

## Clone

```bash
git clone --recurse-submodules https://github.com/dgkngzlr/blog.git
```

Licences of vendored assets: Font Awesome Free (`static/vendor/fontawesome/LICENSE.txt`),
Fira Code (SIL OFL 1.1, https://github.com/tonsky/FiraCode).
