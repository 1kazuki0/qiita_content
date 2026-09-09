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

Rubyでは、`puts "Hello, World"`と1行書いて実行すればすぐ動きました。
しかし、Javaで最初に書く「Hello, World」はこうなります。
```java
public class Main {
  public static void main(String[] args) {
    System.out.println("Hello, World");
  }
}
```
なぜこんなにいっぱい書かないといけないんだ！
呪文のようなこの文章が、Javaでつまずくポイントだったので、
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
この中に、`Main`クラスの内容が書かれています。

# `public static void main(String[] args) {}`
### `public`
さっきと同じで、**どこからでもアクセスできる公開状態**という意味です。

### `static`
「インスタンス（実体、つまりオブジェクト）を作らなくても呼び出せる」という意味です。
Java起動時ではまだ実体がないので、これが無いと最初の入り口として呼べません。

### `void`
このメソッドが**値を返さない**ことを示します。
いわゆる「戻り値なし」のことです。

### `main`
メソッド名です。Java（正確にはJVM）は`main`という決まった名前がないとプログラムが起動しません。
なぜ`main`なのかは後述します。

### `(String[] args)`
`String`は「文字列」を表す型（データの種類）で、後ろの`[]`がつくと、「`String`の配列」つまり、文字列がいくつも並んだリストになります。
`args`はその箱につけた名前（変数名）で、`arguments`（引数）の略です。

### `{}`
**メソッドの始まりと終わりを示すもの**です。
この中に、`main`メソッドの内容が書かれています。

# `System.out.println("Hello, World");`
### `System`
Javaに標準で備わっているクラスです。正確には、インポートなしで使えるクラスです。

### `out`
`System`が持つ「標準出力（画面）」を表すオブジェクトです。
標準出力とは、プログラムが文字を出力する既定の行き先のことで、通常はコンソール（ターミナルやエディタの実行画面）を指します。

### `println`
`out`オブジェクトが持つメソッドで、「1行表示して改行する」メソッド（print + line）です。

### `("Hello, World")`
`println` に渡している引数で、実際に表示したい文字列です。
Javaでは文字列を半角のダブルクォート`" "`で囲むと文字列になる。

# `main`メソッドはプログラムの「入り口」になる
これを説明するには、まずJavaのプログラム実行方法について理解する必要があります。

Javaは「Write Once, Run Anywhere（一度書けば、どこでも動く）」という思想のもと設計されています。
これは、Javaプログラムが`JVM（Java Virtual Machine）`という仮想マシンの上で動作する仕組みになっているため、JVMが各OSの違いを吸収してくれるので、開発者はOSの違いを気にすることなくプログラムを書くことができます。

またJavaは、コンパイル（人間が書いたコードを機械語に翻訳する作業）してから実行する言語なので、
①人間が書いたソースコード（`.java`ファイル）を、
②`javac`というコンパイラ（コンパイルしてくれるプログラム）がバイトコード（`.class`ファイル）に変換し、
③`JVM（Java Virtual Machine）`がバイトコード（`.class`ファイル）を読み取って実行します。

この時、`JVM`は指定されたクラスの`main`メソッドを呼び出し、そこから実行を始めます。
`main`はプログラムの実行が始まる場所、つまり「入り口」なのです。
