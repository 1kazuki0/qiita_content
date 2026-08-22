---
title: ミュータブルとイミュータブルが分からなかったのでRubyで解説
tags:
  - Ruby
  - ミュータブル
  - イミュータブル
private: false
updated_at: ''
id: null
organization_url_name: null
slide: false
ignorePublish: true
posting_campaign_uuid: null
agreed_posting_campaign_term: false
---
# はじめに
paizaのプログラミングスキルチェックを解いていて、変数の代入について深掘りしたところ、ミュータブルとイミュータブルを理解する必要があったので記事にしました。

以下は私が詰まったところの内容です。
a, b, curry, riceには何がはいるでしょうか？

```ruby
a = b = 0
a += 1

p a       # a => [?????]
p b       # b => [?????]

curry = rice = []
curry << "カレー"

p curry   # curry => [?????]
p rice    # rice => [?????]
```
<details><summary>答え</summary>

```ruby
a => 0
b => 1
curry => ["カレー"]
rice => ["カレー"]
```
同じ書き方なのに、整数の`b`は代入されていなくて、配列の`rice`には代入されていました。
この違いの正体が今日のテーマです。

