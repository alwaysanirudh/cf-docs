# Authentication

To get an access token, you must get an partner account created with Capital Float, then Capital Float will generate a set of `CLIENT_ID` and `CLIENT_SECRET` for your app for both the sandbox and live environments. Then, you pass the `CLIENT_ID` and `CLIENT_SECRET` in the request body to acquire an access token.

The authorisation server issues an access token in exchange for your `CLIENT_ID` and `CLIENT_SECRET`. You use the access token for authentication when you make REST API requests by passing it in the Authorization Header.

You can manage your credentials in the Dashboard. All API requests must be made over HTTPS. Any requests made over HTTP will fail.

`Authorization: YOUR_TOKEN`

<aside class="notice">
You must replace <code>YOUR_TOKEN</code> with your access token.
</aside>

> Request:

```shell
# With shell, you can just pass the correct header with each request
curl -X POST \
  <URL>/users/token \
  -H "Content-type: application/json" \
  -d '{"client_id": "<CLIENT_ID>", "client_secret": "<CLIENT_SECRET>"}'
```

> Response:

```json
{
  "access_token": "57ed301af04bf35b40f255feb5ef469ab2f046aff14",
  "expires_in": 7200
}
```

`POST <URL>/users/token`

| Parameter     | Description                   |
| ------------- | ----------------------------- |
| client_id     | Client ID shared with you     |
| client_secret | Client Secret shared with you |

To make a REST API call, you must include request headers including the Authorization header with an access token.