---
title: "かんたんに投稿できるようにした"
date: 2020-12-25T10:04:08+09:00
---

これまではここの記事投稿するときに、Github のリポジトリのページから新しく Markdown ファイル作って～みたいな感じのことをしないといけなくて、ダルさがめちゃめちゃあった。結果としてドラフトがどんどん iPad のなかにたまっていっててアレだったので、ブラウザからシュッっと投稿できるようにした。

ひみつの URL にアクセスすると投稿画面が出てくるみたいな感じで、フォームにタイトルと本文を入れて submit すればオッケーということにした。裏では Flask で作ったサーバが Cloud Run で動いてて、 POST された内容のファイルがこのブログのリポジトリ (github.io) に作成される。あとは Github Actions が動いていい感じに Hugo のビルドが走る。
