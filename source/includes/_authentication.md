# Authentication

To get an access token, you must get an partner account created with Capital Float, then Capital Float will generate a set of `API_KEY` and `API_SECRET` for your app for both the sandbox and live environments. Then, you pass the `API_KEY` and `API_SECRET` in the request body to acquire an access token.

The authorisation server issues an access token in exchange for your `API_KEY` and `API_SECRET`. You use the access token for authentication when you make REST API requests by passing it in the Authorization Header.

You can manage your credentials in the Dashboard. All API requests must be made over HTTPS. Any requests made over HTTP will fail.

`Authorization: YOUR_TOKEN`

<aside class="notice">
You must replace <code>YOUR_TOKEN</code> with your access token.
</aside>

> Request:

```shell
curl -X POST \
  {{url}}/authentication \
  -H "Content-type: application/json" \
  -d '{
    "api_key": "<API_KEY>",
    "api_secret": "<API_SECRET>"
  }'
```

> Response:

```json
{
  "access_token":
    "eyJhbGciOiJIUzUxMiIsInR5cCI6IkpXVCJ9.eyJzY29wZXMiOltdLCJpc3MiOiJzYWZlLmNhcGl0YWxmbG9hdC5jb20iLCJqdGkiOiJlZTRjZDNjMi1lNmU5LTQ3MTAtOWUwMy02NzRlYzFhMjc2MjQiLCJ1c2VyIjp7ImluaXRpYXaN1R9pZCI6MjA2MjMxLCJwYXJ0bmVyX2lkIjo3NiwiY2xpZW50X2lkIjoiMDkwMGRhYjA3NzRmY2YyNjk2OWVmOTE2NzBhMjM1OWMifSwiZXhwIjoxNTI3MTMzNTgyLCJpYXQiOjE1MjQ1NDE1ODIsIm5iZiI6MTUyNDU0MTU4Mn0.x1929FAPE4OxCaMRTKUaoQhSCZ3VhNz3CWatg6LE1IyYRczIoYqLSYXwz3iL3BmwQfdFCrgAYqn-u3CUTxRHpQ",
  "expires_in": 7200
}
```

`POST {{url}}/authentication`

| Parameter  | Description                |
| ---------- | -------------------------- |
| api_key    | API_KEY shared with you    |
| api_secret | API_SECRET shared with you |

To make a REST API call, you must include request headers including the Authorization header with an access token.
