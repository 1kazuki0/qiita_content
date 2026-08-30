---
title: 【Ruby】while文の使い方・使うタイミング
tags:
  - Ruby
  - while
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
Rubyのwhile文をすっかり忘れてしまってたので、復習を兼ねて記事にしました。

# while文とは？

条件が真の間、繰り返し処理を実行します。
いくつか形がありますが、基本形の1に沿って進めます。

```ruby
# 1.基本形
while 条件式
  内容
end

# 2. do付き（doは任意）
while 条件式 do
  内容
end

# 3. 1行（ do または ; で区切る）
while 条件式 do 内容 end
while 条件式 ; 内容; end

# 4. 後置while文
内容 while 条件式

# 5. 後判定while文（条件が偽でも1会実行）
begin
  内容
end while 条件式
```
いくつか形がありますが、基本形の1に沿って進めます。


