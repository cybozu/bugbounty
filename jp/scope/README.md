脆弱性認定ガイドライン
====
サイボウズが脆弱性情報を報告いただいた際に、脆弱性の認定可否を判断する際に使用するガイドラインを公開するレポジトリです。  
ガイドラインの公開前後で認定基準が変更になる場合は、ガイドラインの公開以降に着信したご報告から適用します。

## 認定対象の脆弱性
* [Cross Site Request Forgery （CSRF）](CSRF.md)
* [センシティブな情報の漏洩](SensitiveDataExposure.md)
* [Reflected File Download](ReflectedFileDownload.md)
* [サードパーティ製品の脆弱性](VulnerabilityInThird-partyProducts.md)
* [WordPress の脆弱性](VulnerabilityInWordPress.md)
* [X-Frame-Options:SAMEORIGIN の出力不備](x-frame-options.md)
* [Content Spoofing](ContentSpoofing.md)

上記以外に認定対象としている脆弱性については、以下のドキュメントを参照ください。  
[脆弱性情報ハンドリングポリシー](http://www.slideshare.net/cybozucommunity/ss-30074325/18)  

詳細な認定条件については、今後追加を予定しております。

## 認定対象外の脆弱性
* [CSV Excel Macro Injection（CEMI）](CEMI.md)
* [PDF FormCalc Attack](PDFFormCalcAttack.md)
* [Tabnabbing](Tabnabbing.md)
* [Cross Site Port Attack (XSPA)](XSPA.md)
* [Webブラウザーのリソースに起因する問題](BrowserResources.md)
* [Denial of Service（DoS）](DoS.md)

Copyright (C) Cybozu, Inc
