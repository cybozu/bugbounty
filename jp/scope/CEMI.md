CSV Excel Macro Injection（CEMI）
====

## 脆弱性概要
多くのWebアプリケーションは、ユーザーに対してユーザー設定などのテンプレートをダウンロードすることを許可しています。　
また多くのユーザーはExcel（もしくはLibre OfficeやOpen Office）でCSVファイルを開くことを選択します。
WebアプリケーションがCSVファイルの中身を正しく検証していない場合、セルに入力された内容がマクロとして実行される可能性があります。

CSV Excelマクロインジェクション攻撃は、ユーザーの信頼を悪用した攻撃手法です。
ここでいう「ユーザーの信頼」とは、以下を指します。

1. ユーザーはコンテンツの置いてあるサイトを信頼します
2. ユーザーは（ダウンロードしたファイルが）単なるCSVファイルであること、ファイルに関数やマクロが含まれていないと考えます。

従ってファイル内の潜在的な悪意ある機能についてExcelからの任意の警告を気にとめません。

## 脆弱性の認定可否
認定しない

## 脆弱性として認定しない理由
サイボウズでは他社様の事例として、改修されているケースがあることを確認しています。

> 90131 CSV Excel Macro Injection Vulnerability in export customer tickets
> Zendesk rewarded psychomantis with a $100 bounty for CSV Excel Macro Injection Vulnerability in export customer tickets.
> Zendesk resolved CSV Excel Macro Injection Vulnerability in export customer tickets that was submitted by psychomantis. 
> [CSV Excel Macro Injection Vulnerability in export customer tickets](https://hackerone.com/reports/90131)

この脆弱性が顕在化しないようにするには、製品から出力される CSV データを改変する必要があります。
具体的にはセル内のデータが =, +, - から始まる場合に、セルの先頭にシングルクォートを入れることになるのですが、
そうした場合、CSV の先頭をそれらの文字から始めることができません。この対策方法は、特に "-" (マイナス)については頻出するため、許容することはできないと判断しました。

本件についてマイクロソフト様に Excel の仕様についても伺いましたが、以下のような回答をいただいています。

> ご報告いただきました動作は、ユーザーがマクロを有効にする必要があることから、本件は脆弱性ではないと判断しております。
> 弊社が考えております脆弱性の説明およびセキュリティに関する鉄則は、以下も併せてご参照ください。
> 
> [「セキュリティの脆弱性」の定義](http://technet.microsoft.com/ja-jp/library/gg983510.aspx)
> [セキュリティに関する 10 の鉄則](https://technet.microsoft.com/ja-jp/library/gg983506.aspx#E1)
 
これらを考慮し、最終的には、CSV Excel Macro Injectionの問題を弊社としては脆弱性としては扱わないことといたしました。

## 参考資料
脆弱性概要は、下記資料の日本語抄訳となります。

[CSV Excel Macro Injection](https://www.owasp.org/index.php/CSV_Excel_Macro_Injection)