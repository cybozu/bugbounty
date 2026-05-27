Tabnabbing
====

## 脆弱性概要
「Tabnabbing」はフィッシング攻撃の手法で、2010年にAza Raskin氏によって発表されました。  
[http://www.azarask.in/blog/post/a-new-type-of-phishing-attack/](http://www.azarask.in/blog/post/a-new-type-of-phishing-attack/)

Tabnabbing攻撃の手法は、スクリプトにより、非アクティブのタブ上のページを攻撃用ページ（例：サービスのログイン画面に似せたページ）に書き換え、ユーザがそのタブに移動したとき、攻撃用ページを利用して機密情報（例：ログイン情報）を盗み出すというものです。
下記の条件のいずれかもしくは両方を満たす場合に攻撃が成立します。

* `target="_blank"`が指定されたリンクが攻撃対象のサイト内に存在する
* `window.open()`の記述が攻撃対象のサイト内に存在する

## 脆弱性の認定可否
認定しない

## 脆弱性として認定しない理由
「Tabnabbing」攻撃が可能な箇所について、下記の理由から脆弱性と認定しない方針といたします。

* 主要なブラウザではデフォルトでrel="noopener"として動作するため、被害は限定的であり、リスクを許容できると判断している
[https://caniuse.com/mdn-html_elements_a_implicit_noopener](https://caniuse.com/mdn-html_elements_a_implicit_noopener)

参考までに、Google社では本現象（Phishing by navigating browser tabs）を報奨金の対象としない方針を示しています。  
[https://bughunters.google.com/learn/invalid-reports/web-platform/navigation/5825028803002368/phishing-by-navigating-browser-tabs](https://bughunters.google.com/learn/invalid-reports/web-platform/navigation/5825028803002368/phishing-by-navigating-browser-tabs)

## 参考資料

* [Tabnabbing: A New Type of Phishing Attack](http://www.azarask.in/blog/post/a-new-type-of-phishing-attack/)
* [Phishing by navigating browser tabs](https://bughunters.google.com/learn/invalid-reports/web-platform/navigation/5825028803002368/phishing-by-navigating-browser-tabs)

## 他社商標について
文中に記載されている会社名、システム名、製品名は各社の登録商標または商標です。  
なお、本文中では、「™」、「®」は明記しておりません。
