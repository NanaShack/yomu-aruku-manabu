# 読む・歩く・学ぶ

週に1冊の読書・30,000歩・3時間の勉強を記録する習慣トラッカーです。
サーバーもアカウントも使わず、ブラウザの中だけで動きます。

- 記録は端末のブラウザ（localStorage）に保存されます。外部には送信されません。
- 一度開けばオフラインでも使えます（Service Worker）。
- スマホのホーム画面に追加すると、アプリとして起動できます。
- 「バックアップ」から記録をJSONファイルに書き出し・読み込みできます。

## ファイル

| ファイル | 役割 |
|---|---|
| index.html | アプリ本体（HTML・CSS・JavaScriptを1ファイルに収録） |
| manifest.webmanifest | ホーム画面に追加するための設定 |
| sw.js | オフライン対応 |
| icon.svg / icon-*.png | アイコン |

## 公開のしかた

HTTPSで配信すればどこでも動きます（ビルド不要）。例:

- **GitHub Pages**: このフォルダをリポジトリに置き、Settings → Pages で公開
- **Netlify Drop**: https://app.netlify.com/drop にフォルダをドラッグ＆ドロップ

## 手元で試す

```bash
python3 -m http.server 8000
```

ブラウザで http://localhost:8000 を開きます。
