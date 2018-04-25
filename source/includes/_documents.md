# Documents

## Sanction Docs

Get sanction docs by app_id

> Request:

```shell
curl -X POST \
  {{url}}/documents/ \
  -H "Content-type: application/json"  \
  -H 'Authorization: YOUR_TOKEN' \
  -d '{
    "app_id": "string"
  }'
```

> Response:

If the request was successful

```json
{
    "sanction_letter": "string",
    "nach_mandate": "string",
    "lss": "string",
    "loan_agreement": "string"
}
```

Error responses

```json
{
  "status": -100,
  "message": "Payload is missing app_id"
}
{
  "status": -200,
  "message": "No partner found for current user"
}
{
  "status": -300,
  "message" :"App not found"
}
{
  "status": -400,
  "message" :"Not authorized to view this app"
}
{
  "status": -500,
  "message" :"Sanction not found"
}
```
