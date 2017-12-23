## futaba thread highlighter K
このUserscriptは[himuro\_majika](https://github.com/himuro-majika)氏の[futaba thread highlighter](https://github.com/himuro-majika/futaba_thread_highlighter)を改変したものです。  
ふたば☆ちゃんねるのカタログに現在表示されているすべてのスレ本文の文字列を監視してページトップに一覧表示します。  
一度検索ワードを設定しておけば定時スレ等が探しやすくなります。  
またFirefoxアドオン[KOSHIAN Catarog Marker kai](https://github.com/akoya-tomo/koshian_catalog_marker_kai)との連携で既読スレのピックアップもできます。

Firefoxの場合、[Tampermonkey](https://addons.mozilla.org/ja/firefox/addon/tampermonkey/)を先にインスールしてからスクリプトをインストールして下さい。  
(GreasemonkeyやViolentmonkeyでの動作は未確認です)  
ChromeやOperaでの動作は未確認です。既読スレピックアップ機能が動作しないのでオリジナル版の使用を推奨します。  

※このUserscriptはFirefoxアドオン[KOSHIAN Catarog Marker kai](https://github.com/akoya-tomo/koshian_catalog_marker_kai)との併用を推奨しています。  
[赤福Firefox SP](http://toshiakisp.github.io/akahuku-firefox-sp/)と[ふたクロ](http://futakuro.com/)にも一応対応しているはずですが、オリジナル版の使用を推奨します。

※KOSHIANアドオン改変版は[こちら](https://github.com/akoya-tomo/futaba_auto_reloader_K/wiki)の一覧からどうぞ

## 使い方
* ふたばのカタログモードの設定で「文字数」を適当な大きさ(4以上推奨)に設定してください。(板毎に設定が必要です)
* スレッド検索該当スレッドの[設定]ボタンをクリックして監視したい検索ワードを入力してください。
|で区切ると複数の語句を指定できます。(正規表現使用可。特殊な記号　\\*?+.^$|()[]{}　は全て正規表現のメタキャラクタとして認識されます。)  
検索ワードは全板共通と各板個別でそれぞれ設定できます。  
* (rev1)KOSHIAN Catarog Marker kaiとの連携で既読スレをピックアップできます。（デフォルト：有効）
* (rev1)タブの表示を「板名（二次裏のみサーバー名）＋ソート名（カタログ・新順・古順etc）」に変更します。（デフォルト：有効）
* (rev1)ねないこのNGスレをピックアップしないようにしました。

## インストール
[GreasyFork](https://greasyfork.org/ja/scripts/36639-futaba-thread-highlighter-k)　
[GitHub](https://github.com/akoya-tomo/futaba_thread_highlighter_K/raw/master/futaba_thread_highlighter.user.js)


## 設定
機能の動作はスクリプト冒頭の大文字変数をエディタで編集すれば変更することができます。  

* USE\_BOARD\_NAME:タイトルを板名＋ソート名（カタログ・新順・古順etc）に変更する\(*true*\)  
* USE\_PICKUP\_OPENED\_THREAD:既読ピックアップ機能を使用する（要KOSHIAN Catalog Marker kai v1.1以上）\(*true*\)  
* KOSHIAN\_CATALOG\_MARKER\_STYLE:既読マークのスタイル\(*""*\)  
  - 通常はKOSHIAN Catalog Marker kaiアドオンがマークしたスタイルを自動でコピーしますが、この変数にスタイルを設定すると優先して使用されます。

## 注意事項
* Firefoxアドオン[KOSHIAN Catarog Marker kai](https://github.com/akoya-tomo/koshian_catalog_marker_kai)は必ず**v1.1以上**をインストールしてください。  
（[AMO](https://addons.mozilla.org/ja/firefox/)にあるPachira氏のKOSHIAN 開いたスレをカタログにマークアドオンとは異なるのでご注意下さい）
* 既読スレのピックアップをしない（できない）場合はスクリプト内の設定USE\_PICKUP\_OPENED\_THREADをfalseにしてください。
* Firefoxアドオン[ねないこ](http://nenaiko.sakura.ne.jp/nenaiko/)と併用する場合は、ねないこの設定より「カタログ2」→「カタログ本文のスタイルを指定する」のチェックを外してください。

## 更新履歴
* v1.6.6rev1 2017-12-23
  - KOSHIAN Catarog Marker kaiとの連携で既読スレのピックアップ機能を追加
  - 板名＋ソート名をタブに表示する機能を追加
  - ねないこのNGスレをピックアップしないように変更

***

以下、オリジナル版futaba thread highlighterの更新履歴  

* v.1.6.6 2017-03-04
  - 赤福と合間合間にを同時に使用している場合に該当スレッドの表示が乱れる問題を修正(thanks akoya_tomo)
* v.1.6.5 2017-02-25
  - 赤福の最新に更新で動作しなくなっていた問題を修正
* v.1.6.4 2016-11-13
  - https対応
* v.1.6.3 2016-10-03
  - Firefoxで赤福を使用していない時に初期化ができていなかった問題を修正(thanks iroha ao)
* v.1.6.2 2016-07-17
  - 赤福で「カタログを左寄せ」を有効にしていると動作しない問題を修正
* v.1.6.1 2016-06-04
  - 監視処理の最適化
* v.1.6 2015-12-12
  - 設定画面に区切り文字を挿入ボタンを追加
  - 検索ワードの正規表現の処理を修正
* v1.5 2015-07-07
  - 板毎の検索ワードの設定を追加
  - 削除した検索ワードのハイライトが残ったままになる問題を修正
* v1.4 2015-05-21
  - スタイルの調整
  - アイコン追加
* v1.3 2015-05-19
  - スタイルの調整
* v1.2 2015-05-18
  - スタイルの変更
  - 文字スレがマッチした場合の不具合修正
