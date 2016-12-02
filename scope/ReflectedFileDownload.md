Reflected File Download
====

## 脆弱性概要
Reflected File Download (以下、RFD)はBlack Hat Europe 2014でOren Hafif氏によって発表された攻撃手法です。
(https://www.blackhat.com/docs/eu-14/materials/eu-14-Hafif-Reflected-File-Download-A-New-Web-Attack-Vector.pdf)

RFDは攻撃者に被害者のクライアントPCにおいて、OSレベルでのコマンド実行を可能にする攻撃です。
RFDの攻撃は被害者を信頼されたドメインから攻撃者の用意したリンクに誘導し、悪意のあるファイルをダウンロードさせることで成立します。
被害は信頼されたドメインからダウンロードしたファイルを開くことで、攻撃者が用意したOSコマンド（もしくはスクリプト）を自身のマシンで実行させられます。

Oren Hafif氏によれば、RFDの攻撃が成立する条件として以下の3つが挙げられています。

>For an RFD attack to be successful, there are three simple requirements:

>1)Reflected 
>– some user input is being “reflected” to the response content. This is used to inject shell commands.

>2)Filename
>– the URL of the vulnerable site or API is permissive, and accepts additional input. This is often the case, and is used by attackers to set the extension of the file to an executable extension.

>3)Download
>– the response is being downloaded and a file is created “on-the-fly” by the Web browser. The browser then sets the filename from(2).

1. Reflected 
ユーザーの入力した値がレスポンスの一部に反映される
（シェルコマンドを注入するために使用されます）
2. Filename
サイトもしくはAPIのURLに任意の文字列を追加で入力することが可能である
（多くの場合、攻撃者がファイルの拡張子を実行可能な形式に設定するために使用されます）
3. Download
レスポンスの中身がWebブラウザを介しファイルとして、ダウンロードされる
（Webブラウザは、ファイル名を攻撃者が入力した任意の文字列から設定します）

（Oren Hafif　Reflected File Download a New Web Attack Vector, 2014 p.4, 訳は引用者による)

## 脆弱性の認定可否
認定する

## 脆弱性に対する対策が必要な個所 (Scope)
脆弱性概要に記載したRFDの要件をすべて満たす箇所を、RFDの脆弱性として認定します。

但し、同一のロジックが別の処理で利用され、複数の箇所で脆弱性が顕在化しているなど、いくつかのケースにおいては類似の脆弱性として扱わせていただく場合があります。
詳細は[報奨金獲得に関するガイドライン](https://cybozu.co.jp/company/security/bug-bounty/guideline.pdf)をご参照ください。

## 参考資料
* [Reflected File Download a New Web Attack Vector](https://www.blackhat.com/docs/eu-14/materials/eu-14-Hafif-Reflected-File-Download-A-New-Web-Attack-Vector-wp.pdf)