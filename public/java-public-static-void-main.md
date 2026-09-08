---
title: java-public-static-voidってなに？
tags:
  - Java
  - 初学者
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
Rubyの勉強を経て、現在Javaの学習を始めました。

Rubyでは、`puts "Hello"`と1行書いて実行すればすぐ動きました。
しかし、Javaで最初に書く「Hello, World」はこうなります。
```java
public class Main {
  public static void main(String[] args) {
    System.out.println("Hello, World");
  }
}
```
なぜこんなにいっぱい書かないといけないんだ！
呪文のようなこの文章が、Javaでつまづくポイントだったので、
1単語ずつ分解してみました。

# `public class Main {}`

### `public`
**どこからでもアクセスできる公開状態**という意味。
アクセス修飾子と呼ばれています。
<details><summary>アクセス修飾子とは？</summary>

「どこから使えるかを決めるルール」で、プログラムが大きくなると、外から触って欲しくない部分が出てきます。それを制御するための仕組みです。
```java
public     // 誰でもどこからでも使える
private    // 同じクラスの中だけ
protected  // 同じパッケージと継承先だけ
```
</details>

### `class`
**クラスを定義する宣言**です。Javaはオブジェクト指向言語なので、基本的にクラスの中に処理を記載します。

### `Main`
**クラスの名前**です。`class Main`で「Mainという設計図を作る」という意味です。
これは、ファイル名と一致させる必要があります。
`public class Main`の場合は、`Main.java`ファイルでないといけません。

### `{}`
**クラスの始まりと終わりを示すもの**です。
この中に、クラスの内容が書かれています。
