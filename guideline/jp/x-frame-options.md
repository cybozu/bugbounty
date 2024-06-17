X-Frame-Options:SAMEORIGIN の出力不備
====
## 脆弱性概要
レスポンスヘッダに `X-Frame-Options: SAMEORIGIN` が付与されていない場合、クリックジャッキングに利用される可能性があります。  
本稿では、API のレスポンスにおける `X-Frame-Options: SAMEORIGIN` の出力について、認定の可否に関する方針を記載します。

### クリックジャッキングとは
> ウェブサイトの中には、ログイン機能を設け、ログインしている利用者のみが使用可能な機能を提供しているものがあります。該当する機能がマウス操作のみで使用可能な場合、細工された外部サイトを閲覧し操作することにより、利用者が誤操作し、意図しない機能を実行させられる可能性があります。このような問題を「クリックジャッキングの脆弱性」と呼び、問題を悪用した攻撃を、「クリックジャッキング攻撃」と呼びます。

（https://www.ipa.go.jp/security/vuln/websecurity/clickjacking.html より引用）

## 脆弱性の認定可否
認定する

## 脆弱性に対する対策が必要な個所 (Scope)
クリックジャッキングによる機密性・完全性・可用性のいずれかの侵害につながる処理  
ただし、影響がないと考えられる箇所に関しては、この限りではありません。

## 例外として認定しないケース
### Webサイトの脆弱性に関して
Webサイトと製品では、脆弱性の認定基準が異なります。  
そのため、下記URLの弊社Webサイトにおいて、レスポンスヘッダに`X-Frame-Options: SAMEORIGIN`が付与されていなくても、脆弱性としては扱いません。  
[https://cybozu.co.jp/products/bug-bounty/#web-site](https://cybozu.co.jp/products/bug-bounty/#web-site)

## 参考資料
[Clickjacking](https://www.owasp.org/index.php/Clickjacking)  
[X-Frame-Options レスポンスヘッダ](https://developer.mozilla.org/ja/docs/Web/HTTP/X-Frame-Options)  
