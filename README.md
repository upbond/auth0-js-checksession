Forked from [auth0/auth0.js](https://github.com/auth0/auth0.js/blob/master/example/index.html)

---

### Log in

To log in to a specific organization, pass the ID or name as the `organization` parameter when creating the `WebAuth` client:

```js
const webAuth = new WebAuth({
  domain: '{YOUR_UPBOND_DOMAIN}',
  clientID: '{YOUR_UPBOND_CLIENT_ID}'
});
```

---

## Run the Sample

To run this sample locally, you can use the `serve` package:

```bash
npm install -g serve
serve -s .
```

Then, open your browser and go to:

```
http://localhost:3000
```

---

## How to Test Session

You can use this sample to check whether you have an active session using UPBOND's SSO capabilities:

1. **Run the sample** with `serve -s .`
2. **Open** `http://localhost:3000` in your browser.
3. At the **bottom of the page**, you'll see a **Session Config** section.
4. **Fill in** only the `domain` and `clientID` fields, then click **Update**.
5. In a **new browser tab**, go to GSID mypage and **log in**.

---

[auth0/auth0.js](https://github.com/auth0/auth0.js/blob/master/example/index.html) からフォーク

---

### ログイン

特定の組織にログインするには、`WebAuth` クライアントを作成する際に `organization` パラメータとしてIDまたは名前を指定します：

```js
const webAuth = new WebAuth({
  domain: '{YOUR_UPBOND_DOMAIN}',
  clientID: '{YOUR_UPBOND_CLIENT_ID}'
});
```

---

## サンプルの実行方法

このサンプルをローカルで実行するには、`serve` パッケージを使用します：

```bash
npm install -g serve
serve -s .
```

その後、ブラウザで以下のURLを開いてください：

```
http://localhost:3000
```

---

## セッションのテスト方法

このサンプルを使って、UPBONDのSSO機能を利用したアクティブなセッションがあるかどうかを確認できます：

1. `serve -s .` を使ってサンプルを**起動**します。
2. ブラウザで `http://localhost:3000` を**開きます**。
3. ページの**一番下**に「**Session Config**」セクションがあります。
4. `domain` と `clientID` フィールド**のみ入力**し、**Update** をクリックします。
5. **新しいブラウザタブ**でGSIDのマイページにアクセスして**ログイン**します。
6. サンプルページに戻り、「**Check if you have an active session**」セクションまでスクロールします。
7. **Check Session** をクリックします。

セッションが有効であれば、結果としてユーザー情報が表示されます。

> ⚠️ **重要**: このサンプルは、ブラウザでサードパーティCookieが有効になっていないと動作しません。セッション検出を正しく行うために、必ず有効になっていることをご確認ください。
7. Return to the sample page and scroll to the **"Check if you have an active session"** section.
8. Click **Check Session**.

If the session is active, you should see your user information appear in the result.

> ⚠️ **Important**: This sample will not work unless third-party cookies are enabled in your browser. Please make sure they're allowed for proper session detection.
