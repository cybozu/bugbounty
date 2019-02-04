X-Frame-Options:SAMEORIGIN の出力不備
====
## 脆弱性概要
レスポンスヘッダに X-Frame-Options: SAMEORIGIN が付与されていない場合、クリックジャッキングに利用される可能性があります。  
本稿では、API のレスポンスにおける X-Frame-Options: SAMEORIGIN の出力について、認定の可否に関する方針を記載します。

### クリックジャッキングとは
> クリックジャッキング攻撃とは、ユーザを視覚的にだまして正常に見えるウェブページ上のコンテンツをクリックさせ、別のウェブページのコンテンツをクリックさせる攻撃のことである。その結果、ユーザが公開するつもりのないプライバシー情報を公開させられたり、意図しない情報を登録させられたりするなどの被害を受ける可能性がある

（https://www.ipa.go.jp/files/000026479.pdf より引用）

## 脆弱性の認定可否
認定する

## 脆弱性に対する対策が必要な個所 (Scope)
クリックジャッキングによる機密性・完全性・可用性の侵害につながる処理  
ただし、影響がないと考えられる箇所に関しては、この限りではありません。

## 参考資料
[Clickjacking](https://www.owasp.org/index.php/Clickjacking)  
[X-Frame-Options レスポンスヘッダ](https://developer.mozilla.org/ja/docs/Web/HTTP/X-Frame-Options)  
[IPAテクニカルウォッチ 知らぬ間にプライバシー情報の非公開設定を公開設定に変更されてしまうなどの『クリックジャッキング』に関するレポート](https://www.ipa.go.jp/about/technicalwatch/20130326.html)
