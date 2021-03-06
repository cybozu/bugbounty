オープンリダイレクト
===

## 脆弱性概要
オープンリダイレクトとは、任意のリダイレクト先を指定できることで意図しないURLに遷移させることができる脆弱性です。  
これにより、信頼できるWebサイトのURLを装い、不正なWebサイトへリダイレクトさせることが可能になります。

## 脆弱性の認定可否
認定する

## 脆弱性に対する対策が必要な個所 (Scope)
ユーザーの入力によって、処理が実行された後のリダイレクト先を製品の意図しないURLに指定できる場合に脆弱性と認定します。 

## 例外として認定しないケース
リクエストヘッダの一部を書き換えた場合に発生するオープンリダイレクトに関しては認定いたしません。

## 参考資料
[これなら合格！ 正しいリダイレクターの作り方 (1/3)：HTML5時代の「新しいセキュリティ・エチケット」（4）](https://www.atmarkit.co.jp/ait/articles/1406/20/news007.html)
