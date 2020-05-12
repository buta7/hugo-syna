# README

以下が404 Not Foundになるが github pagesでは"_"で始まるファイルが閲覧不可か?

https://higebobo.github.io/hugo-syna/_index/hero/logo.svg

## セットアップ

サイト作成

```shell
hugo new site hugo-syna
```

レポジトリ初期化

```shell
cd hugo-syna
git init
echo '*.bak' >> .gitignore
echo '*~' >> .gitignore
echo '*.orig' >> .gitignore
echo 'public' >> .gitignore
```

テーマ設定

```shell
cd themes 
git submodule add https://github.com/okkur/syna.git
```

サイト設定

```shell
cd hugo-syna
cp -pr ./themes/syna/exampleSite/{*.toml,static,content} .
```

config.toml

```toml
baseURL = "/hugo-syna"
title = "Hugo Syna"
languageCode = "ja"
publishDir = "docs"
defaultContentLanguage = "ja"
theme = "syna"
themesDir = "./themes"
```

Githubレポジトリ作成後

```shell
git remote add origin git@github.com:higebobo/hugo-syna.git
hugo
git add -A
git commit -m 'init'
git push -u origin master
```

Github>Settings>Gighub Pages>Source>master branch/docs folder

## 使い方

総合的なウェブサイトなので詳細はcontent参照のこと

## Github連携

config.tomlに以下の設定があることを確認

```toml
baseURL = "/hugo-syna"
publishDir = "docs"
```

公開(githubにプッシュ)

```shell
make deploy
```

## Link

* [Syna \| Hugo Themes](https://themes.gohugo.io/syna/)
