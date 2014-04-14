# Mobile Safari のURLスキーム動作 #

* 同一URLのタブは使いまわされる
* 開いていないURLが指定されたら新規タブで開く

## おまけ ##

### Safariは、Window.close()で自タブを閉じれない ###

かわりに以下の処理を使えば閉じれる。

```
  window.opener = window;
  var win = window.open(location.href, "_self");
  win.close();
```
