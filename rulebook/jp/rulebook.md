脆弱性報奨金制度ルールブック
===
# 0. はじめに
サイボウズ株式会社脆弱性報奨金制度(以下、本制度)は、サイボウズが提供するサービスに存在するゼロデイ脆弱性を早期に発見し改修することを目的とする制度です。本制度に基づき脆弱性を発見し、弊社に報告される方（以下、報告者）には、弊社サービスの品質向上にご協力いただいた謝礼として、報奨金をお支払いいたします。  
報奨金制度の実施期間は、サイボウズ脆弱性報奨金制度([https://cybozu.co.jp/products/bug-bounty/](https://cybozu.co.jp/products/bug-bounty/))のページをご覧ください。

# 1. 検証対象サービス
本制度の検証対象となるサービスは、サイボウズ脆弱性報奨金制度([https://cybozu.co.jp/products/bug-bounty/](https://cybozu.co.jp/products/bug-bounty/))のページをご覧ください。各サービスの最新バージョンを、本制度の対象といたします。サービスの詳細につきましては、製品ホームページをご覧ください。
# 2.報告規約
以下の条件を満たした方は、本制度に基づき脆弱性情報を報告し、報奨金を獲得することができます。
- 報告時においてサイボウズまたはサイボウズの子会社の従業員ではないこと
- 報告時において業務委託契約、出向契約、派遣契約等の契約形態により、サイボウズまたはサイボウズの子会社の業務に従事していないこと
- 過去にサイボウズまたはサイボウズの子会社において正社員として雇用されていないこと
- 過去にサイボウズまたはサイボウズの子会社において製品開発及びクラウドサービスの運用関連の業務に従事していないこと
- 日本語または、英語で Cy-PSIRT とコミュニケーションできること
- 脆弱性報奨金制度規約 に同意いただけること

脆弱性報奨金制度規約については、以下をご覧ください。  
https://cybozu.co.jp/products/bug-bounty/pdf/terms.pdf

# 3. コミュニケーション
## 3.1	問い合わせ
本制度は、サイボウズ株式会社 Cy-PSIRTが運営しています。  
本制度における脆弱性報告に関するお問い合わせは、報告用サイトにて受け付けます。報告用サイトのアカウントをお持ちでない方は、報告用サイトアカウントお申し込みフォームよりお申し込みください。  

報告用サイト：  
https://cy-bugbounty.cybozu.com/k/  
報告用サイトアカウントお申し込みフォーム：  
https://form.kintoneapp.com/public/form/show/d16726f3de2ce25f846c43603fe7260c80a5adbc1ed878a7fcd66f8b671be525  

その他のお問い合わせはメールでも受け付けます。  
メール：  
productsecurity@cybozu.co.jp

## 3.2	PGP 鍵
報告者が Cy-PSIRT に連絡する際には、PGP 鍵を利用できます。公開鍵の情報は以下をご覧ください。  
https://www.cybozu.com/jp/features/management/cy-psirt.asc


# 4. サイボウズの脆弱性情報ハンドリングポリシー
報告された脆弱性情報は、サイボウズの「脆弱性情報ハンドリングポリシー」に沿って受け付けます。脆弱性情報ハンドリングポリシーとは、サイボウズが提供する製品および、サービスで脆弱性が発見された場合にどのように取り扱い、公開するかを定めたものです。詳細は以下の資料をご覧ください。  
https://cybozu.co.jp/company/security-policy/

# 5. 脆弱性情報の対応プロセス
## 5.1 対応プロセス
報告者が脆弱性情報をCy-PSIRTに連絡した場合、以下のプロセスで脆弱性情報を評価します。

1.	「対応番号」を割り振り、報告者に連絡します。
2.	報告内容を元に、脆弱性に該当するかどうか及び報奨金額を算出します。
3.	評価結果を連絡します。
- 本制度の対象サービスに存在する挙動のうち、脆弱性に該当すると弊社が判断することを「認定」と呼びます。また、その時点を認定日とします。
- 認定の可否が決定次第、報告者に結果を連絡します。
- 認定の可否を決定するための情報が不足している場合、報告者に追加の情報提供を依頼する場合があります。
- この時点では、評価及びお支払いする金額が変動する可能性があります。
4.	報告者がCy-PSIRTに「対応完了」の連絡をし、対応プロセスが完了します。
- Cy-PSIRTが評価結果を連絡する際に、返信期日を記載します。その期日までに、報告者から返信がない場合も、対応プロセスは完了となります。
- この時点でお支払いする金額は本確定となり、これ以降お支払い金額は変更されません。

## 5.2	受付順序について
受信したお問い合わせについて、報告された順に受け付けます。

## 5.3	対応時間について
脆弱性の報告及びお問い合わせの受付時間は平日の10:00 – 17:00(JST)です。
受信したご連絡について、原則として 2 営業日以内に受け付けます。

## 5.4	評価順序について
原則として「対応番号」の若い順に評価を行いますが、脆弱性の報告状況などにより評価順序が入れ替わることがあります。

# 6. 報奨金
## 6.1	お支払い金額の計算式
報奨金は、以下のルールに基づいて確定します。

### 製品・サービス
|項目|概要|ケース|計算方法|
|--|--|--|--|
|1|RCEか否か|RCE|100万円(固定)、計算式4～5が適用されます。|
|||RCE以外|計算式2～5が適用されます。|
|2|脆弱性種別|SQLインジェクション|6～25万円|
|||インジェクション（SQLインジェクションは除く|2～10万円|
|||アクセス制御の不備|2～30万円|
|||入力確認の不備|2～25万円|
|||XSS|4～6.5万円|
|||上記以外|1～30万円|
|3|製品による係数|kintone<br>kintone モバイル<br>cybozu.com 共通管理<br>cybozu.com 運用基盤|×5|
|||Garoon|×2　※オプション製品は含まれません|
|||上記以外|×1|
|4|上限の計算||製品ごとで1件の脆弱性につき100万円|
|5|支払先による上乗せ|報告者|×1|
|||寄付|×2|

### ホームページ
|項目|概要|ケース|計算方法|
|--|--|--|--|
|1|RCEか否か|RCE|100万円(固定)|
|||RCE以外|2万円(固定)|
|2|お支払先による上乗せ|報告者|×1|
|||寄付|×2|

## 6.2	報奨金獲得ルールの補足
|項目|概要|ルール|
|--|--|--|
|1|調査結果により複数の脆弱性が認定された|報告いただいた脆弱性に応じた報奨金は獲得できますが、報告内容を基にCy-PSIRTで調査した結果、同一製品または他製品で脆弱性が検出された場合、それらに対する報奨金は獲得できません。|
|2|同一要因・類似の脆弱性が報告された|同一製品で、同一要因または類似の脆弱性情報を報告いただいた場合、先に報告された脆弱性情報を脆弱性として認定します。認定された報告者のみ報奨金を獲得できます。|
|3|既知の脆弱性が報告された|弊社がすでに認識している脆弱性情報を報告いただいた場合、報奨金は獲得できません。|
|4|動作環境外の脆弱性が報告された |	動作環境外で再現する脆弱性を報告いただいた場合、報奨金は獲得できません。動作環境については各製品のホームページを確認してください。
|5|調査の結果、評価結果が変更された場合|一度認定された脆弱性情報について、調査の結果評価結果が変更された場合、対応プロセスが完了していない場合にかぎり、変更後の評価内容に応じて報奨金も変更されます。|

### 6.2.1	同一要因とする脆弱性の例
- パラメータから入力した場合と、ハッシュから入力した場合の双方で脆弱性が顕在化する
- 同一のサーバーで稼働しているホームページで、環境設定に起因する脆弱性が顕在化する
- 同一のロジックまたは関数を利用しているなどが原因で、同一製品内の異なる箇所で脆弱性が顕在化する

なお、同一要因の脆弱性でも、製品が異なる場合には、この規則を適用しないこととします。

### 6.2.2	類似した脆弱性の例
- 製品内に類似のロジックが分散していることが原因で、複数の異なる箇所で同様の脆弱性が顕在化する

なお、類似した脆弱性でも、製品が異なる場合には、この規則を適用しないこととします。

## 6.3	報奨金の受け渡しについて

報告者が報告した脆弱性情報の対応プロセスが完了した場合、翌々月末に報奨金を現金でお振込みします。  
報告者は Cy-PSIRT に、振込先情報を連絡する必要があります。なお、法人口座への入金には対応しておりません。  
振込先情報を連絡いただけない場合、または連絡いただいた送金先情報をもとに弊社が送金手続を行ったにもかかわらず報告者が報奨金を受領できなかった場合、お支払いの手続きに時間を要する、またはお支払いができない場合がございます。

## 6.4	報奨金の寄付について
報告者は報奨金を獲得する代わりに、獲得した報奨金をサイボウズが指定する OSS コミュニティに寄付することが可能です。報告者が報奨金を寄付することを選択した場合、獲得した金額と同額をサイボウズが上乗せし、OSS コミュニティに寄付いたします。なお、「報奨金の獲得」と「寄付」を組み合わせることはできません。

### 6.4.1	サイボウズが指定する寄付先について
- Apache Software Foundation 
- Linux Foundation
- 日本にあるOWASP Local Chapter

寄付先のご指定が無い場合、Apache Software Foundation に寄付いたします。

### 6.4.2	寄付の詳細について
報告者の方から寄付する旨ご連絡を受けたのち、2ヶ月以内に報告者の方が指定した団体にサイボウズが寄付いたします。寄付者の名義は「サイボウズ株式会社」となります。寄付が完了した時点で、報告者の方にCy-PSIRTからご連絡いたします。税制上の優遇処置などのために、書面を発行するなどの業務はお受けできません。日本国内の方の場合、今回の寄付先は税制優遇処置を受けることが出来ない団体であることを確認しております。

## 6.5	税金について
報告者が獲得した報奨金額が特定の金額を超える場合、報告者はご自身で確定申告を行う義務が発生いたします。確定申告に関する詳細につきましては、以下の国税庁のホームページ、「No.1900　給与所得者で確定申告が必要な人」および、「No.1490　一時所得」をご覧ください。   
http://www.nta.go.jp/taxes/shiraberu/taxanswer/shotoku/1900.htm  
http://www.nta.go.jp/taxes/shiraberu/taxanswer/shotoku/1490.htm  

支払調書は確定申告書に添付する必要がないため、発行しません。  
報告者は他に収入がなくても、税務上の扶養から外れることがあります。なお、健康保険の扶養に関しては、影響しません。扶養控除に関する詳細につきましては、以下の国税庁のホームページ、「No.1180　扶養控除」をご覧ください。  
https://www.nta.go.jp/taxes/shiraberu/taxanswer/shotoku/1180.htm  

国によって税制度は異なるため、税制度に関しては各自でお調べください。

# 7. ポイント
## 7.1 付与ポイントの計算

報告いただいた内容に応じて、報告者は、報奨金とは別にポイントを獲得できます。  
※以下はポイントの参考値であり、実際の獲得ポイントは弊社で決定いたします。  
※各項目の合計値を獲得できます。  
※その他弊社が有益な情報と判断した場合には、状況に応じてポイントが付与されます。  

|項目| ケース| 詳細 | ポイント|
|--|--|--|--|
|1| 製品・サービスの脆弱性(RCEは除く)|製品・サービスの脆弱性が報告された| 10～40 |
| | ホームページの脆弱性(RCEは除く) | ホームページの脆弱性が報告された<br>※以降の2と3は適用されません。	|10|
|	|RCE|RCEの脆弱性情報が報告された|40|
|2| 再現手順の的確さ|報告内容をもとに弊社で決定いたします。|0 or 10|
3|影響範囲の明確さ|報告内容をもとに弊社で決定いたします。|0 or 10|
|4|cybozu.com運用基盤への影響あり|対象製品が「cybozu.com運用基盤」である|10|
|5|Cybozu賞|年に１度報告内容のうち、弊社で「社内影響度」「緊急度」「インパクト」などを総合的に判断し、選出いたします。<br>※決定したタイミングでポイントが付与されます。|100|
## 7.2	ポイント獲得特典について
獲得ポイントが以下のいずれかを満たしたタイミングでCy-PSIRTから特典を送付します。
- 対象年度中の獲得ポイントの合計が100ptに達した
- 対象年度中の獲得ポイントの合計が300ptに達した  
※特典は先着順です。報奨金制度の実施期間終了後に条件を満たした場合、特典を送付しないことがあります。
- 対象年度末の獲得ポイントのランキング上位3名に入った  
※送付対象者は、暫定値を以って決定されることがあります。

報告者はそれぞれの条件を満たすことにより、それぞれの特典を獲得可能です。
なお、特典の送付時期は諸般の事情により遅れる可能性があります。

## 7.3	その他
- ポイントは弊社で評価結果を作成する段階で、暫定値として付与されます。この時点では、評価の変更により増減することがあります。その後、対応プロセスが完了した時点でポイントが確定します。
- 対応プロセスが完了後、いかなる場合においてもポイントは変更しません。
- 総獲得ポイントは、実施年度ごとに集計されます。実施年度を跨ぎません。
- ポイントの現金またはその他物品への交換はできません。

# 8.謝辞
本制度に基づき脆弱性を発見し、報告いただいた方には、弊社サービスの品質向上にご協力いただいた感謝を込めて、報告者のお名前を「サービスの品質向上にご協力いただいた皆様」ページに掲載いたします。謝辞の掲載条件及び掲載時期の詳細は、以下のページをご覧ください。
https://cybozu.co.jp/products/bug-bounty/specialthanks/

# 9.本ルールブックの変更
サイボウズは、事前に公表することなく、本ルールブックの変更を行うことがあります。
本ルールブックの重要部分に変更があった場合は、サイボウズは報告者に対しその内容を通知します。

# 10. 検証環境について
検証環境提供プログラムページをご覧ください。
https://cybozu.co.jp/products/bug-bounty/#TestingEnvironmentProgram