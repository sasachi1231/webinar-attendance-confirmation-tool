# Webinar attendance confirmation tool

ニフクラ mobile backend(以下、NCMB)を使ったウェビナーの出席確認ができるurlの生成並びに出席結果の確認ができるツール。

## 必要物

- NCMBのアカウント
    - https://mbaas.nifcloud.com/
- NCMB JavaScript SDK
    - https://github.com/NIFCLOUD-mbaas/ncmb_js
    - v3.0.2がこのリポジトリに含まれていますが、より新しいバージョンのSDKがリリースされている場合↑↑のリポジトリからncmb.min.jsを落としてきてください。

## 使い方

### NCMBのアプリ作成

NCMBで新規アプリを作成し、アプリケーションキーとクライアントキーを控えてください。

### api_key.jsの編集

api_key.jsを開いて、'YOUR_APPLICATION_KEY'、'YOUR_CLIENT_KEY'、'YOUR_APPLICATION_ID'をそれぞれ作成したアプリのアプリケーションキー、クライアントキー、アプリケーションIDに置き換えてください。  
※アプリケーションIDは、NCMB管理画面で該当アプリを開いた際のURLに https://console.mbaas.nifcloud.com/#/applications/ `アプリケーションID` の部分です。

### ファイルストアへのアップロード

NCMBのファイルストアへ以下ファイルをアップロードし、公開ファイル設定を有効にしてください。

- index.html
- ncmb.min.js
- setting.html
- api_key.js

### ウェビナー準備

settings.htmlにアクセスし、画面に従って情報を入力し、urlを生成してください。  

![settings.html](/1.png)

生成後、NCMBのデータストアに先程入力した情報でクラスが作成されているので、CSVエクスポートの上、urlをご利用ください。

![データストア画面(開催前)](/2.png)

### 参加者確認

ウェビナー終了後、先程作成したクラスを確認すると、attendanceフィールドが作成され、出席情報が記載されています。

![データストア画面(開催後)](/3.png)

## ライセンス

MIT License
