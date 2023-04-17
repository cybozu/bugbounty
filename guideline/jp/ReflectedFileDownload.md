Reflected File Download
====

## 脆弱性概要
Reflected File Download（以下、RFD）はBlack Hat Europe 2014でOren Hafif氏によって発表された攻撃手法です。
[https://www.blackhat.com/docs/eu-14/materials/eu-14-Hafif-Reflected-File-Download-A-New-Web-Attack-Vector.pdf](https://www.blackhat.com/docs/eu-14/materials/eu-14-Hafif-Reflected-File-Download-A-New-Web-Attack-Vector.pdf)

RFDは攻撃者に被害者のクライアントPCにおいて、OSレベルでのコマンド実行を可能にする攻撃です。  
RFDの攻撃は被害者を信頼されたドメインから攻撃者の用意したリンクに誘導し、悪意のあるファイルをダウンロードさせることで成立します。  
被害は信頼されたドメインからダウンロードしたファイルを開くことで、攻撃者が用意したOSコマンド（もしくはスクリプト）を自身のマシンで実行させられます。  

Oren Hafif氏によれば、RFDの攻撃が成立する要件として以下の3つが挙げられています。

1. Reflected - ユーザーの入力した値がレスポンスの一部に反映される（シェルコマンドを注入するために使用されます）
2. Filename - 脆弱なサイトのURLまたはAPIが追加の文字列を許容する（多くの場合、攻撃者がファイルの拡張子を実行可能な形式に設定するために使用されます）
3. Download - レスポンスの中身がWebブラウザを介しファイルとして、ダウンロードされる（ブラウザは(2)で指定されたファイル名を設定します）

## 脆弱性の認定可否
認定する

## 脆弱性に対する対策が必要な個所 (Scope)
脆弱性概要に記載したRFDの要件をすべて満たす箇所を、RFDの脆弱性とします。  

但し、RFDのうちダウンロード時にファイル名および拡張子を改竄することができるようなものについては、報奨金制度の対象として今後追加の認定はいたしません。  
この場合、脆弱性は改修しないものとして内容を公開してもよいこととします。  
拡張子やファイル名を書き換えることが可能という現象によって直接的な影響は増えない為、影響が小さいと評価しております。  

* サイボウズ製品を利用しているユーザーの場合、製品の機能として任意のファイルをアップロードが可能である
* サイボウズ製品を利用しているユーザーではない場合、フィッシング等により特定のファイルをアップロードさせるための手段が必要になる

なお、ダウンロード時にファイルの内容を書き換えることが可能な RFD については、新規の脆弱性として認定いたします。

同一のロジックが別の処理で利用され、複数の箇所で脆弱性が顕在化しているなど、いくつかのケースにおいては類似の脆弱性として扱わせていただく場合があります。  
詳細は[脆弱性報奨金制度ルールブック](https://github.com/cybozu/bugbounty/blob/master/rulebook/jp/rulebook.md)をご参照ください。

## 参考資料
RFDの攻撃が成立する要件についての記述は、下記資料の日本語抄訳となります。
* [Reflected File Download a New Web Attack Vector](https://www.blackhat.com/docs/eu-14/materials/eu-14-Hafif-Reflected-File-Download-A-New-Web-Attack-Vector-wp.pdf)
