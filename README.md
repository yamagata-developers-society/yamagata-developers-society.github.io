# jekyll-redirect-template

This is a template that makes access to top page of GitHub pages redirect to arbitrary url.

- - -

Github Pagesのトップページへのアクセスを任意のURLにリダイレクトするためのテンプレートプロジェクトです。

主に以下のユースケースを想定しています。

- Github PagesのデフォルトURLで運用していたウェブサイトを他のURLに移転したため、Github Pagesへのアクセスを移転先のURLへリダイレクトしたい。

## 使い方

1. このリポジトリをクローンします。

```bash
$ clone https://github.com/succi0303/jekyll-redirect-template
```

`index.html`の`{url you want to redirect to}`の部分をリダイレクト先のURLに書き換えます。

- 編集前

```markdown
---
layout: redirected
sitemap: false
permalink: /
redirect_to: {url you want to redirect to}
---
```

- 編集後

```markdown
---
layout: redirected
sitemap: false
permalink: /
redirect_to: https://blog.succi0303.com
---
```

2. 変更をコミットしてGithub Pages用のリポジトリ・ブランチにプッシュします。

```bash
$ git add .
$ git commit -m "Change redirect url"
```

- ユーザーページの場合

```bash
$ git remote add gh-pages-origin https://github.com/{username}/{username}.github.io.git
$ git push -u gh-pages-origin master
```

- プロジェクトページの場合

```bash
$ git remote add gh-pages-origin https://github.com/{username}/{username}.github.io.git
$ git checkout -b gh-pages
$ git push -u gh-pages-origin gh-pages
```

## 動作イメージ

下記ののリンクをクリックすると`https://blog.succi0303.com`にリダイレクトされます。

- [https://succi0303.github.io](https://succi0303.github.io)

## 制限事項

リダイレクトされるのはトップページへのアクセスのみです。

サブディレクトリや個別のページへの直接アクセスには404が返ります。
