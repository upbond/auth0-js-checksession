Forked from [auth0/auth0.js](https://github.com/auth0/auth0.js/blob/master/example/index.html)

## Table of Contents

- [Passwordless Login](#passwordless-login)
- [Organizations](#organizations)
- [WebAuth.client.login(options, callback)](#webauthclientloginoptions-callback)
- [Run the Sample](#run-the-sample)

---

### Log in to an organization

To log in to a specific organization, pass the ID or name as the `organization` parameter when creating the `WebAuth` client:

```js
const webAuth = new WebAuth({
  domain: '{YOUR_UPBOND_DOMAIN}',
  clientID: '{YOUR_UPBOND_CLIENT_ID}'
});
```

You can also specify an organization when calling `authorize`:

```js
webAuth.authorize({
  organization: '{YOUR_UPBOND_ORGANIZATION_ID_OR_NAME}'
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
5. In a **new browser tab**, go to `https://id.grand-seiko.com` and **log in**.
6. Return to the sample page and scroll to the **"Check if you have an active session"** section.
7. Click **Check Session**.

If the session is active, you should see your user information appear in the result.

> ⚠️ **Important**: This sample will not work unless third-party cookies are enabled in your browser. Please make sure they're allowed for proper session detection.
