脆弱性認定ガイドライン
====
サイボウズが脆弱性情報を報告いただいた際に、脆弱性の認定可否を判断する際に使用するガイドラインを公開するレポジトリです。  
ガイドラインの公開前後で認定基準が変更になる場合は、ガイドラインの公開以降に着信したご報告から適用します。

## 認定対象の脆弱性
* [Cross Site Request Forgery （CSRF）](CSRF.md)
* [センシティブな情報の漏洩](SensitiveDataExposure.md)
* [Reflected File Download](ReflectedFileDownload.md)
* [サードパーティ製品の脆弱性](VulnerabilityInThird-partyProducts.md)
* [WordPressの脆弱性](VulnerabilityInWordPress.md)
* [X-Frame-Options:SAMEORIGIN の出力不備](x-frame-options.md)
* [Content Spoofing](ContentSpoofing.md)
* [XSS（クロスサイトスクリプティング）](XSS.md)
* [オープンリダイレクト](OpenRedirect.md)

上記以外に認定対象としている脆弱性については、以下のドキュメントを参照ください。  
[脆弱性情報ハンドリングポリシー](http://www.slideshare.net/cybozucommunity/ss-30074325/18)  

詳細な認定条件については、今後追加を予定しております。

## 認定対象外の脆弱性
* [CSV Injection](CSVInjection.md)
* [PDF FormCalc Attack](PDFFormCalcAttack.md)
* [Tabnabbing](Tabnabbing.md)
* [Cross Site Port Attack (XSPA)](XSPA.md)
* [Webブラウザーのリソースに起因する問題](BrowserResources.md)
* [大量のデータやリクエストを必要とするDenial of Service（DoS）](DoS.md)
* [中間者攻撃が前提となる脆弱性](man-in-the-middle.md)
* [エスケープシーケンスインジェクション](escape-sequence-injection.md)

Copyright (C) Cybozu, Inc
