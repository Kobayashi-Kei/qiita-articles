---
title: はじめてのGitHub Copilot Free
tags:
  - "AI"
  - "AIコーディングエージェント"
  - "Github Copilot"

private: true
updated_at: ""
id: null
organization_url_name: null
slide: false
ignorePublish: false
---

# new article body

# はじめに

昨今は、Cursor や Cline、Github Copilot など複数の AI コーディングエージェントが登場しており、それらを活用して爆速でアプリを開発できる時代が来ています。
しかしながら、私はまだそれらのツールをしっかり使ったことがありませんでした。（さすがに危機感）
そこでこの記事では、筆者が初めて Github Coplot を使ってみた所感をまとめます。

# 導入方法

[VS Code で GitHub Copilot 無料版の導入　備忘録](https://zenn.dev/yuta_haruna/articles/fb809e68e6bae5)を参考に、VS Code で GitHub Copilot Free を導入しました。

# Github Copilot Chat について

私のイメージでは、Copilot はガシガシコード補完を行なって開発を進めていくイメージだったのですが、この Copilot Chat で対話をしながら開発を進めるのがいいようです。

GitHub Copilot の 3 つのモード（Ask, Edit, Agent）があり、以下のように使い分けることができます。

- **Ask**: 質問をして、回答を得るモード。簡単な質問をするのに適しています。
- **Edit**: コードの修正を依頼するモード。プロジェクト内の編集したいファイルに対して編集内容を指示することで、コードの修正を行います。
- **Agent**: コードの実行を依頼するモード。Copilot が自律的に手順を生成し、コマンドを実行したりファイルを編集したりします。

今回は一番サポートが手厚そうな Agent モードを使いながら、実際にアプリを作ってみたいと思います。

# 使ってみた

## 作成するアプリについて

まずは今回作りたいアプリの要件を簡単に考えます。事前に Gemini の API を使ったアプリを使いたいと思っていたので、要件も含めて以下のようなプロンプトとしました。

```
以下のサイトの情報を参考にGEMINIを使った料理の献立提案アプリを作りたい。

以下はgeminiのAPIの利用方法の参考にね
https://qiita.com/zukki2/items/10bfeb1c4330aa18ff87

要件
・Webアプリ
・トップページには今日の気分を入力するテキストボックスと送信ボタン
・送信すると、気分に合わせたおすすめの献立を提案する
・推薦する献立の候補は事前にファイルで保存した情報とネット上の情報を組み合わせる
・献立は高タンパク低脂質が基本
```

![スクリーンショット 2025-06-04 17.58.45.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/1665105/bca0d70a-98f0-4228-8770-37a5fcf86b00.png)

![スクリーンショット 2025-06-04 18.00.22.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/1665105/4402a189-939f-4a90-8325-e3bc5da2ca9f.png)
