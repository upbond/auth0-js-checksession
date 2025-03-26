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

Open your browser to the printed local address to see the login demo in action.