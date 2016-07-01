# 脆弱性名
Cross Site Request Forgery（CSRF）

# 脆弱性概要
クロスサイトリクエストフォージェリ（以下、CSRF）とは、現在認証されている Web アプリケーション上で、
ユーザーが意図しない行動を強制させる攻撃です。
具体的には CSRF 攻撃は状態が変化するリクエストを対象とします。
攻撃者は被害者に強制したレスポンス内容を確認する方法がないため、データを窃取することはありません。
Email やチャットを介してリンクを送るといったソーシャルエンジニアリング技法の助けを借りて、
攻撃者は Webアプリケーションのユーザーをだまし、攻撃者の選択したアクションを実行させることができます。
被害者が一般ユーザー権限を持つ場合、CSRF 攻撃は、資金を転送したり、Email アドレスを変更する
といった状態を変化させるリクエストをユーザーに強制することができます。
被害者が管理者権限を持つ場合、CSRF 攻撃は、Web アプリケーション全体を危険にさらすことになります。

# 脆弱性の認定可否
認定する

# 脆弱性に対する対策が必要な個所（Scope）
データに変更を及ぼす処理について、CSRF 対策を必要とします。
具体的には下記の処理です。

* ユーザーのログイン
* サーバー内データおよびユーザーの認証を変更するAPI

下記の処理は対象外となります。

* ログアウト処理
* GETで副作用的にデータの変更がある API（例：通知の既読処理）
* UI の状態を保持するためのデータを変更する API（例：フォルダの開閉処理）
※ アクセス権に関連する設定を除く

# 参考資料
脆弱性概要は、下記資料の日本語抄訳となります。

Cross-Site Request Forgery (CSRF)
[https://www.owasp.org/index.php/Cross-Site_Request_Forgery_(CSRF)]
