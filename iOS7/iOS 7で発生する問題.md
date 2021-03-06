iOS 7で発生する問題
=================

## iOS 7の変更点 ##

### Standaloneモードでステータスバーがコンテンツにかぶる ###

"apple-mobile-web-app-status-bar-style"の指定によってはステータスバーが視認できなくなる。

**指定なし or "default"：**  
　ステータスバーの領域が黒一色で塗りつぶされる。

**"black-translucent"：**  
　フォント色が白で背景透明のステータスバーとなり、コンテンツが下にまわり込む。  
　ページの背景やコンテンツによっては非常に見栄えが悪いので、考慮が必要。

**"black"：**  
　iOS 6までのDefaultと同じ見た目になる。黒背景に白文字。  
　

### SafariとStandaloneのCookie、Storage、Cacheが別管理になった ###

iOS 6まではSafariとStandalone間でCookieが共有されていたが、iOS 7ではそれぞれ個別の管理になっている様子。  
StorageとCacheも同様


## バグと思われる挙動 ##

### Standaloneモードでalertが表示されない（〜 iOS 7.0.3） ###
デバッグする際は要注意  
→iOS 7.1 で修正済み

### Standaloneモードでアプリ連携出来ない（〜 iOS 7.0.2） ###
→iOS 7.0.3で修正された


### Standaloneモードでプリンタ出力できない（〜 iOS 7.0.2） ###
→iOS 7.0.3で修正された


### キーボード表示中にローテーションすると表示が崩れる（〜 iOS 7.1） ###

ローテーション時に謎の黒い領域があらわれ、コンテンツが正しくレイアウトされない。  
→iOS7.0.3以降、standaloneモードでは発生しない。Safariモードでは7.1でも発生する


### ローテーションするとページ上部がUIにめり込む（〜 iOS 7.0.3） ###

Portrait→Landscapeのローテーション時に、
DocumentHeightが表示領域よりも大きくなり、ページの上部がSafariのUIの下に隠れる  
→iOS 7.1 で修正済み ただし、Landscape時にdocumentHeightが20px(CSS)長いのは直ってない


### マルチタスク切替画面でStandaloneモードのWebアプリの向きが常にPortraitになる（〜 iOS 7.0.3） ###
→iOS 7.1 で修正済み
