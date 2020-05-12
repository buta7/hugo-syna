# README

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
baseURL = "https://higebobo.github.io/hugo-syna/"
title = "Hugo Syna"
languageCode = "ja"
publishDir = "docs"
defaultContentLanguage = "ja"
theme = "syna"
themesDir = "./themes"
```

> baseURLのプロトコルは例外を除いてhttpsにすること

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
baseURL = "https://higebobo.github.com/hugo-syna/"
publishDir = "docs"
```

公開(githubにプッシュ)

```shell
make deploy
```

## Link

* [Syna \| Hugo Themes](https://themes.gohugo.io/syna/)
