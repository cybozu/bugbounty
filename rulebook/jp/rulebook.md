脆弱性報奨金制度ルールブック
===
# 0. はじめに
サイボウズ株式会社脆弱性報奨金制度(以下、本制度)は、サイボウズが提供するサービスに存在するゼロデイ脆弱性を早期に発見し改修することを目的とする制度です。本制度に基づき脆弱性を発見し、弊社に報告される方（以下、報告者）には、弊社サービスの品質向上にご協力いただいた謝礼として、報奨金をお支払いいたします。  
なお、日本語版と英語版に内容の差異がある場合は、日本語版の記述を優先します。

# 1. 検証対象サービス
本制度の検証対象となるサービスは、次のWebサイトをご覧ください。
[https://cybozu.co.jp/products/bug-bounty/#product-service](https://cybozu.co.jp/products/bug-bounty/#product-service)   
各サービスの最新バージョンを、本制度の対象といたします。サービスの詳細につきましては、各製品のWebサイトをご覧ください。

# 2. 報告規約
以下の条件をすべて満たした方は、本制度に基づき脆弱性情報を報告し、報奨金を獲得することができます。
- 報告時においてサイボウズまたはサイボウズの子会社の従業員ではないこと
- 報告時において業務委託契約、出向契約、派遣契約等の契約形態により、サイボウズまたはサイボウズの子会社の業務に従事していないこと
- 報告日の過去1年間にサイボウズまたはサイボウズの子会社において正社員として雇用されていないこと
- 報告日の過去1年間にサイボウズまたはサイボウズの子会社において製品開発及びクラウドサービスの運用関連業務に従事していないこと
- 日本語または、英語でCy-PSIRTとコミュニケーションできること
- 脆弱性報奨金制度規約に同意いただけること

脆弱性報奨金制度規約については、以下をご覧ください。  
https://cybozu.co.jp/products/bug-bounty/pdf/terms.pdf

# 3. コミュニケーション
## 3.1	問い合わせ
本制度は、サイボウズ株式会社 Cy-PSIRTが運営しています。  
本制度における脆弱性報告に関するお問い合わせは、報告用サイトにて受け付けます。報告用サイトのアカウントをお持ちでない方は、報告用サイトアカウントお申し込みフォームよりお申し込みください。  

報告用サイト：  
https://cy-bugbounty.cybozu.com/k/  
報告用サイトアカウントお申し込みフォーム：  
https://cy-psirt.form.kintoneapp.com/public/d16726f3de2ce25f846c43603fe7260c80a5adbc1ed878a7fcd66f8b671be525   

その他のお問い合わせは以下のフォームよりお問い合わせください。  
脆弱性報告を除くお問い合わせフォーム：  
https://cy-psirt.form.kintoneapp.com/public/inquery  

## 3.2	PGP鍵
報告者がCy-PSIRTに連絡する際には、PGP鍵を利用できます。公開鍵の情報は以下をご覧ください。  
https://www.cybozu.com/jp/features/management/cy-psirt.asc

# 4. サイボウズの脆弱性情報ハンドリングポリシー
報告された脆弱性情報は、サイボウズの「脆弱性情報ハンドリングポリシー」に沿って受け付けます。脆弱性情報ハンドリングポリシーとは、サイボウズが提供する製品および、サービスで脆弱性が発見された場合にどのように取り扱い、公開するかを定めたものです。詳細は以下の資料をご覧ください。  
https://cybozu.co.jp/company/security-policy/

# 5. 脆弱性情報の対応プロセス
## 5.1 対応プロセス
報告者が脆弱性情報をCy-PSIRTに連絡した場合、以下のプロセスで脆弱性情報を評価します。

1. Cy-PSIRTが「対応番号」を割り振り、報告者に連絡します。
2. Cy-PSIRTは報告内容を基に、認定可否の判断(※1)を行います。認定の場合は、あわせて報奨金額の算出を行います。
3. Cy-PSIRTは、報告者に評価結果を連絡します。
4. 報告者がCy-PSIRTに「対応完了」の連絡をし、対応プロセスが完了します。(※2)  

※1 本制度の対象サービスに存在する挙動のうち、報奨金支払い対象の脆弱性にあたると弊社が判断することを「認定」と呼び、その時点を認定日とします。また、認定の可否を決定するための情報が不足している場合、報告者に追加の情報提供を依頼する場合があります。  
※2 Cy-PSIRTが評価結果を連絡する際に、返信期日を記載します。その期日までに報告者から返信がない場合も、対応プロセスは完了となります。

結果のご連絡の時点では、評価及びお支払いする金額が変動する可能性があります。  
対応プロセス完了時に、報奨金額は確定します。同一要因による別の挙動のご報告があっても、追加で報奨金はお支払いしません。
例外として、追加報告された挙動による影響が大きいと弊社で判断した場合は、再評価を行い報奨金の差額をお支払いすることがあります。

## 5.2	受付順序について
受信したお問い合わせについて、報告された順に受け付けます。

## 5.3	対応時間について
脆弱性の報告及びお問い合わせの受付時間は平日の10:00 – 17:00(JST)です。  
受信したご連絡について、原則として 3 営業日以内に受け付けます。   
ただし、年末年始等の長期休暇を挟む場合は通常よりお時間をいただく場合がございます。

## 5.4	評価順序について
原則として「対応番号」の若い順に評価を行いますが、脆弱性の報告状況などにより評価順序が入れ替わることがあります。

# 6. 報奨金
## 6.1	お支払い金額
報奨金は、以下のルールに基づいて確定します。  
寄付を選択する場合は、お支払いする報奨金が2倍になります。詳細は「6.4　報奨金の寄付について」を確認してください。

### 製品・サービス
||kintone(\*1)<br>cybozu.com 共通管理(\*1)<br> cybozu.com Store<br>kintone アプリストア|Garoon(\*1)<br>メールワイズ<br>Office|cybozu.com 運用基盤<br>セキュアアクセス<br>Cybozu Desktop2(Windows版)|
|:--|:--|:--|:--|
|RCE|200万円(固定)|200万円(固定)|200万円(固定)|
|SQLインジェクション|40-160万円|10-100万円||
|XSS|10-40万円|5-20万円||
|アクセス制御の不備|20-80万円|5-40万円||
|モバイルアプリ特有の脆弱性|1-200万円<br>（対象：kintoneモバイル）|1-200万円<br>（対象：クラウド版 Garoon モバイル、サイボウズ Office モバイル）||
|その他|1-200万円|1-200万円|1-200万円|

(\*1)各製品が提供するAPIを含む


### Webサイト
|項目|概要|ケース|金額|
|--|--|--|--|
|1|RCEか否か|RCE|100万円(固定)|
|||RCE以外|2万円(固定)|

報奨金制度対象のWebサイトは以下の「対象となる製品・サービスおよびWebサイト」をご確認ください。  
[https://cybozu.co.jp/products/bug-bounty/#product-service](https://cybozu.co.jp/products/bug-bounty/#product-service)

## 6.2	報奨金獲得ルールの補足
|項目|概要|ルール|
|--|--|--|
|1|調査結果により複数の脆弱性が認定された|複数の脆弱性を報告いただいた場合、それらに応じた報奨金を獲得できます。ただし、報告内容を基にCy-PSIRTで調査した結果、同一製品または他製品で脆弱性が検出された場合、それらに対する報奨金は獲得できません。|
|2|同一要因の脆弱性が報告された|同一製品で、同一要因の脆弱性情報を報告いただいた場合、先に報告された脆弱性情報を脆弱性として認定します。認定された報告者のみ報奨金を獲得できます。|
|3|既知の脆弱性が報告された|弊社がすでに認識している脆弱性情報を報告いただいた場合、報奨金は獲得できません。|
|4|動作環境外の脆弱性が報告された |	動作環境外で再現する脆弱性を報告いただいた場合、報奨金は獲得できません。動作環境については各製品のWebサイトを確認してください。
|5|調査の結果、評価結果が変更された場合|調査の結果、評価結果が変更された場合、対応プロセスが完了していない場合にかぎり、変更後の評価内容に応じて報奨金も変更されます。|

### 6.2.1	同一要因とする脆弱性の例
- パラメータから入力した場合と、ハッシュから入力した場合の双方で脆弱性が顕在化する
- 同一のサーバーで稼働しているWebサイトで、環境設定に起因する脆弱性が顕在化する
- 同一のロジックまたは関数を利用しているなどが原因で、同一製品内の異なる箇所で脆弱性が顕在化する

なお、同一要因の脆弱性でも、製品が異なる場合には、この規則を適用しないこととします。

### 6.2.2 報奨金をお支払いできない報告
以下の内容に当てはまる報告は、原則として認定および報奨金のお支払いをすることはできません。
1. [脆弱性認定ガイドライン](https://github.com/cybozu/bugbounty/tree/master/guideline/jp)の「認定対象外の脆弱性」に当てはまる脆弱性を含んだ報告
2. 具体的な脅威や、報告対象となっている箇所が不明な報告（例：自動で脆弱性を探索するプログラムの出力結果を貼り付けただけの報告）

ただし、上記のうち1. に当てはまる場合でも、弊社が重要な報告であると判断した場合はその限りではありません。

## 6.3	報奨金の受け渡しについて

対応プロセスがすべて完了した時点から、翌々月末に報奨金を現金でお振込みします。  
報告者は Cy-PSIRT に、振込先情報を連絡する必要があります。指定可能な振込先は規約をご確認ください。  
振込先情報を連絡いただけない場合、または連絡いただいた送金先情報をもとに弊社が送金手続を行ったにもかかわらず報告者が報奨金を受領できなかった場合、お支払いの手続きに時間を要する、またはお支払いができない場合がございます。

## 6.4	報奨金の寄付について
報告者は報奨金を獲得する代わりに、獲得した報奨金を弊社が指定するOSSコミュニティに寄付することが可能です。報告者が報奨金を寄付することを選択した場合、獲得した金額と同額をサイボウズが上乗せし、OSS コミュニティに寄付いたします。なお、「報奨金の獲得」と「寄付」を組み合わせることはできません。

### 6.4.1	サイボウズが指定する寄付先について
- Apache Software Foundation 
- Linux Foundation
- 日本にあるOWASP Local Chapter

寄付先のご指定が無い場合、Apache Software Foundation に寄付いたします。

### 6.4.2	寄付の詳細について
報告者の方から寄付する旨ご連絡を受けたのち、報告者の方が指定した団体にサイボウズが寄付いたします。寄付者の名義は「サイボウズ株式会社」となります。　  
寄付が完了した時点で、報告者の方にCy-PSIRTからご連絡いたします。  
税制上の優遇処置などのために、書面を発行するなどの業務はお受けできません。日本国内の方の場合、今回の寄付先は税制優遇措置を受けることが出来ない団体であることを確認しております。

## 6.5	税金について
報奨金を獲得した報告者は、各国の制度に基づき申告が必要になる場合があります。  
国によって税制度は異なるため、制度に関してはご自身で調査し、対応してください。  
なお、支払調書は確定申告書に添付する必要がないため、発行しません。  

# 7. ポイント

## 7.1 付与ポイントの計算

報告者は報告いただいた内容などに応じて、報奨金とは別にポイントを獲得できます。  
以下はポイントの参考値であり、実際の獲得ポイントは弊社で決定いたします。  
下記以外にも弊社が有益な情報と判断した場合など、状況に応じてポイントが付与されます。  

### 7.1.1 報告により獲得できる基本ポイント

|項目| ケース| 詳細 | ポイント|
|--|--|--|--|
|1| 製品・サービスの脆弱性(RCEは除く)|製品・サービスの脆弱性が報告された| 10～40 |
| | Webサイトの脆弱性(RCEは除く) | Webサイトの脆弱性が報告された<br>※以降の2と3は適用されません。	|10|
|	|RCE|RCEが報告された|40|
|2| 再現手順の的確さ|報告内容をもとに弊社で決定いたします。|0 or 10|
3|影響範囲の明確さ|報告内容をもとに弊社で決定いたします。|0 or 10|
|4|cybozu.com運用基盤への影響あり|「cybozu.com運用基盤」へ影響のある脆弱性情報が報告された|10|
|5|Cybozu賞|年に１度報告内容のうち、弊社で「社内影響度」「緊急度」「インパクト」などを総合的に判断し、選出いたします。<br>※決定したタイミングでポイントが付与されます。また、ポイントは選出された報告ごとに付与されます。複数の報告が選ばれる可能性もございます。|100|

報告以外にもイベントへの参加や検証実績に応じてポイントを付与する場合があります。

### 7.1.2 ランク倍率

過去の検証や報告の実績に応じてランクが設けられています。基本ポイントにランクごとに設定されている倍率を乗じたポイントを獲得することができます。

|ランク名|ランク条件|倍率|
|--|--|--|
|Platinum|以下の条件をすべて満たす。<br>直近1年間での報告数が20件以上<br>直近1年間の報告により獲得した基本ポイント数の合計が400pt以上|2.0|
|Gold|以下の条件をすべて満たす。<br>直近1年間での報告数が10件以上<br>直近1年間の報告により獲得した基本ポイント数の合計が200pt以上|1.8|
|Silver|以下の条件をすべて満たす。<br>直近1年間の報告数が1件以上<br>直近3ヶ月間の検証環境へのアクセス数の平均が100以上|1.5|
|Bronze|上記以外|1.0|

ランクの変動は月末時点の情報で判定され翌月上旬頃に適用されます。報告のタイミングにかかわらずポイントが付与されるタイミングでのランク倍率が適用されます。  


## 7.2	ポイント獲得特典

報告者は獲得ポイント数に応じて弊社が定めるリストの中の賞品と交換することができます。  
交換希望者は、Cy-PSIRT に送付先情報を連絡する必要があります。送付先をご連絡いただいた後、配送手続きを進めます。  
配送先により配送に時間がかかる場合や、配送できない場合がございます。  
また、ポイントと交換した賞品により確定申告が必要になる場合があります。その場合も「6.5 税金について」に準じるものとします。

## 7.3 リアルタイムポイントランキング

獲得したポイント数のランキングが弊社SNSなどで公開されます。  
ランキングの表示名は指定していただくか、匿名からお選びいただけます。

## 7.4	その他

- 獲得したポイントは、報告用サイトのアカウントを削除した場合、または獲得から3年が経過した月末以降に順次失効します。失効後のポイントはご利用いただけませんのでご了承ください。
- 本ポイント制度は「9.本ルールブックの変更」に準じて内容が変更される場合があります。また運営上の都合によりポイント制度を停止または終了する場合があります。停止または終了する場合、その影響及び本ポイント制度の運営状況などに照らし、適切な期間と方法により情報提供を行います。

# 8. 謝辞
本制度に基づき脆弱性を発見し、報告いただいた方には、弊社サービスの品質向上にご協力いただいた感謝を込めて、報告者のお名前を「サービスの品質向上にご協力いただいた皆様」ページに掲載いたします。謝辞の掲載条件及び掲載時期の詳細は、以下のページをご覧ください。
[https://cybozu.co.jp/products/bug-bounty/specialthanks/](https://cybozu.co.jp/products/bug-bounty/specialthanks/)

# 9. 本ルールブックの変更
サイボウズは、事前に公表することなく、本ルールブックの変更を行うことがあります。
本ルールブックの重要部分に変更があった場合は、サイボウズは参加者に対しその内容を通知します。　　

# 10. 検証環境について
検証環境提供プログラムページをご覧ください。
[https://cybozu.co.jp/products/testing-environment/](https://cybozu.co.jp/products/testing-environment/)
