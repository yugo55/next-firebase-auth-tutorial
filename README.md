# Next.js + FirebaseでAuthenticationチュートリアル
## 備忘録
### 手順
1. Firebaseで新しいプロジェクトを作成し、メールとパスワードによる方法を有効にする。
2.  [プロジェクト設定] > [サービス アカウント]に移動し、 [新しい秘密キーを生成]からjsonファイルをダウンロード。
3.  next.jsプロジェクトを作成。
4.  .env.localファイルを作成し、環境変数を設定。
5.  next-firebase-auth-edgeをインストールし、config.tsファイルに初期設定を記述。
6.  middleware.tsファイルを作成し、ミドルウェアを追加。
7.  app/page.tsxファイルを記述。
8.  firebaseをインストールし、firebase.tsファイルを作成し、FirebaseクライアントSDKを初期化。
9.  app/register/page.tsxファイル、app/login/page.tsxファイル、app/HomePage.tsxファイルを記述。

### ポイント
- 環境変数FIREBASE_ADMIN_PRIVATE_KEYの値を間違えると以下のエラーが発生する。
  ```
  Error [ERR_HTTP_HEADERS_SENT]: Cannot append headers after they are sent to the client
    at ServerResponse.appendHeader (node:_http_outgoing:689:11)
    at AsyncLocalStorage.run (node:async_hooks:346:14)
  digest: "1075671692"
  ```
  FIREBASE_ADMIN_PRIVATE_KEYには「-----BEGIN PRIVATE KEY-----」や「\n」も記述する。

## 参考サイト
https://hackernoon.com/ja/%E6%9C%80%E6%96%B0%E3%81%AE-nextjs-%E6%A9%9F%E8%83%BD%E3%81%A7-Firebase-%E8%AA%8D%E8%A8%BC%E3%82%92%E4%BD%BF%E7%94%A8%E3%81%99%E3%82%8B
