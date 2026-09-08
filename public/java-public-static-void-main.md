---
title: java-public-static-voidってなに？
tags:
  - ''
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
呪文のようなこと文章が、Javaでつまづくポイントだったので、
1単語ずつ分解してみました。

