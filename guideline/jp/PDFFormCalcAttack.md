PDF FormCalc Attack
====

## 脆弱性概要
「PDF FormCalc Attack」はAdobe社が開発した演算言語であるFormCalcを利用した攻撃手法で、
APPSEC EU 2015でAlexander Inführ氏によって公開されました。  
[https://2015.appsec.eu/wp-content/uploads/2015/09/owasp-appseceu2015-infuhr.pdf](https://2015.appsec.eu/wp-content/uploads/2015/09/owasp-appseceu2015-infuhr.pdf)

攻撃の要点はFormCalcを利用すると、PDFファイルがアップロードされているオリジンで任意のリクエストを発行できることです。  
上記を悪用することで、被害者ユーザーのCookieやCSRF対策用トークンを付与したリクエストを送信することが可能となり、攻撃者のサイトを閲覧したユーザーの権限で、任意のコードが特定の製品で実行される可能性があります。

攻撃を受ける可能性があるユーザーの条件は以下です。  

1. 任意のpdfをアップロード可能な機能を有するアプリケーションを利用している  
2. Adobe PDF Reader Plugin を Microsoft Internet ExplorerもしくはMozilla Firefoxで有効にしている  

クロスオリジンでリクエストを送信できる問題（CVE-2014-8453、CVE-2022-28244）はAdobe社によって修正されています。  
但し同一オリジン内でリクエストを送信できる点については、Adobe社より、脆弱性としない見解をいただいています。  

> From our perspective, website owners must realize that PDF is active content, and serving user-uploaded/malicious PDFs from a non-throwaway domain is effectively an XSS (just like hosting an arbitrary/malicious HTML). 

## 脆弱性の認定可否
認定しない

## 脆弱性として認定しない理由
本現象は Sandbox Domain にユーザーコンテンツを格納することで、一定程度リスクを軽減できます。  
Google 社をはじめ著名なサービスを展開する多くの企業が上記を実装済みあることを認識しています。  

一方、サイボウズ製品はユーザーがアップロードしたコンテンツをプログラムが動作するオリジンと同一オリジンに格納する仕様です。  
本仕様を改めるには、非互換な仕様変更が必要となります。このような変更は、ユーザーの負担が大きくなります。  
とりわけオンプレミス版をご利用中のお客様にとっては、別オリジンにユーザーが格納するコンテンツを配置する設定を行うことが困難です。  

結論として、再現する条件が限定的（他社製品を利用していることが攻撃の前提条件となる）ことも踏まえ、本件は制限事項として扱う方針とします。  
以下の Webページにて、お客様へご案内いたしております。  

* [cybozu.com制限事項](https://www.cybozu.com/jp/service/restrictions.html)  
* [Adobe Acrobat Reader Pluginの利用について（2016/11/11）](https://cs.cybozu.co.jp/2016/006288.html)  

Microsoft Internet ExplorerもしくはMozilla Firefoxをご利用中のお客様には、Acrobat Reader Pluginが有効になっている場合は無効化することを推奨いたします。
設定の確認および方法については以下をご確認ください。

* [Internet Explorer 11 のアドオンを管理する](https://support.microsoft.com/ja-jp/help/17447/windows-internet-explorer-11-manage-add-ons)  
* [Firefox のプラグインを使用するには](https://support.mozilla.org/ja/kb/use-plugins-play-audio-video-games)

## 参考資料
* [JVNTA#94087669 細工された PDF による情報詐取について](https://jvn.jp/ta/JVNTA94087669/)
* [Hack Patch!-PDF特殊機能（FormCalc編）](https://shhnjk.blogspot.jp/2016/10/pdfformcalc.html)  
* [InsertScript-Multiple PDF Vulnerabilities - Text and Pictures on Steroids](http://insert-script.blogspot.jp/2014/12/multiple-pdf-vulnerabilites-text-and.html)

## 他社商標について
文中に記載されている会社名、システム名、製品名は各社の登録商標または商標です。  
なお、本文中では、「™」、「®」は明記しておりません。