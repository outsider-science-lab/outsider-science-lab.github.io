+++
title = "富岳向けにRustをコンパイルして動作させる"
description = "まずはHello worldが動くのを確認"
date = 2022-08-16T08:20:00+09:00
updated = 2024-10-29T08:20:00+09:00
draft = false
weight = 10
sort_by = "weight"
template = "docs/page.html"

[extra]
lead = "実際に富岳でRustを使って Hello world! と印字するまでの方法を紹介します。"
toc = true
top = false
+++

## リポジトリ

実際に動かしてみるデモのソースコードはこちらにあります。

- [outsider-science-lab/hello-rust-of-fugaku: Hello world! of Fugaku, in Rust.](https://github.com/outsider-science-lab/hello-rust-of-fugaku)

## 事前準備

シェルはbashを想定しています。ログインノードまでsshができるという前提で以下話を進めていきます。Fortran/C/C++は書いたことがあればベターですが、書いたことがなくても問題ありません。

### rust toolchain

[rustinit](https://www.rust-lang.org/tools/install)を利用して、自分の環境にRustの環境は構築しておいてください。

この時のツールチェインとして、以下のものが選べます：

- `aarch64-unknown-linux-musl`
- `aarch64-unknown-linux-gnu`

デフォルトのツールチェインをそれぞれに設定しても構いませんし、複数入れたうえで `.cargo/config` 以下に次のように記述して、プロジェクトごとに使い分けることもできます。

```toml
[build]
target = "aarch64-unknown-linux-gnu"
```

（以下工事中…）
