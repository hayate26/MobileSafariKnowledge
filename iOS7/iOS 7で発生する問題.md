iOS 7で発生する問題
=================

Mobile Safari向けのWebサイトやWebアプリを作るにあたって役立つ情報をまとめます。

####表記について

**Standaloneモード**

```<meta name="apple-mobile-web-app-capable" content="yes" />```を指定してSafariのUIを非表示にしたモードのことは"Standaloneモード"もしくは"Standalone"と表記します。フルスクリーンモードとかアプリモードとか色々な呼び方がありますが、検索しづらいので統一します。

---------

### iOS 7の変更点

#### Standaloneモードでステータスバーがコンテンツにかぶる

"apple-mobile-web-app-status-bar-style"を指定しない、もしくは"default"指定した場合、iOS7ではフォントカラーが白で背景透明（コンテンツがまわりこむ）のステータスバーとなります。
ページの背景やコンテンツによっては非常に見栄えが悪いので、考慮が必要。

**対策**

"apple-mobile-web-app-status-bar-style"に、"black"を指定する。これでiOS 6までのDefaultと同じ見た目になる。



---------

### バグと思われる挙動

#### Standaloneモードでアプリ連携出来ない（iOS 7.0.2）
→iOS 7.0.3で修正された

#### Standaloneモードでプリンタ出力できない（iOS 7.0.2）
→iOS 7.0.3で修正された

#### キーボード表示中にローテーションすると表示が崩れる（iOS 7.0.3）

ローテーション時に謎の黒い領域があらわれ、コンテンツが正しくレイアウトされない。

#### ローテーションするとページ上部がUIにめり込む（iOS 7.0.3）

Portrait→Landscapeのローテーション時に、
DocumentHeightが表示領域よりも大きくなり、ページの上部がSafariのUIの下に隠れる

#### ステータスバーがコンテンツの裏に隠れる（iOS 7.0.3）

"apple-mobile-web-app-status-bar-style"を"black-translucent"と指定すると、ステータスバーがページの裏に隠れる。ページを下にスライドすると見えるが、指を離すとページがバウンスして戻るので隠れる。仕様？


------
