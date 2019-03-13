# jekyll-redirect-template

This is a template project that makes access to GitHub Pages redirect to arbitrary URL.

For the situation illustrated below.

> You had hosted a website at GitHub Pages and you moved the site to other URL. You want to make accesses to old URL redirect to new URL.

## Usage

1. Clone this repository.

```bash
$ clone https://github.com/succi0303/jekyll-redirect-template.git
```

2. Replace `{redirect url}` in `index.html` with your redirect URL.

- before

```markdown
---
layout: home
redirect_to: {redirect url}
---
```

- after

```markdown
---
layout: home
redirect_to: https://blog.succi0303.com
---
```

3. Replace `{redirect url}` in `404.html` with your redirect URL.

- before

```markdown
---
layout: default
redirect_to: <redirect url>
---
```

- after

```markdown
---
layout: default
redirect_to: https://blog.succi0303.com
---
```

4. Commit the changes and push into your GitHub Pages repository/branch.

```bash
$ git add .
$ git commit -m "Set redirect URL"
```

- For user page

```bash
$ git remote add gh-pages-origin https://github.com/{username}/{username}.github.io.git
$ git push -u gh-pages-origin master
```

- For project page

```bash
$ git remote add gh-pages-origin https://github.com/{username}/{username}.github.io.git
$ git checkout -b gh-pages
$ git push -u gh-pages-origin gh-pages
```

## Exmaple

Following link redirects to `https://blog.succi0303.com`.

- [https://succi0303.github.io](https://succi0303.github.io)
