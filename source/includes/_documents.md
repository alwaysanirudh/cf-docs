# Documents

## Fetch files

Fetch files by appid

> Request:

```shell
curl -X GET \
  {{url}}/documents/files?appid={{appid}} \
  -H "Content-type: application/json"  \
  -H 'Authorization: YOUR_TOKEN' \
```

> Response:

```json
If the request was successful

{
  "sresp": [
    {
      "path": "string",
      "size": 1,
      "name": "string",
      "tags": [
        "string"
      ]
    }
  ],
  "status": 1
}
```

`GET {{url}}/documents/files?appid={{appid}}`

## Doc List

Fetch files by appid

> Request:

```shell
curl -X GET \
  {{url}}/documents/list?appid={{appid}} \
  -H "Content-type: application/json"  \
  -H 'Authorization: YOUR_TOKEN' \
```

> Response:

```json
If the request was successful

{
  "SectionName": {
    "TagName": [
      {
        "path_name": "string",
        "extra_tag_name": "string",
        "ts": "string",
        "tags": "string",
        "synced": 0,
        "extra_tag_id": 0,
        "size": null,
        "id": 0,
        "filename": "string"
      }
    ]
  }
}
```

`GET {{url}}/documents/list?appid={{appid}}`

## Upload File

Upload file

> Request:

```shell
curl -X POST \
  {{url}}/documents \
  -H 'content-type: multipart/form-data; boundary=----WebKitFormBoundary7MA4YWxkTrZu0gW' \
  -F appid=af2118a7-9333-4c36-88d2-b4afdaa682fb \
  -F 'tags=Co:Recent Utility/Landline bill' \
  -F 'file=@/filepath/pan.png'
```

> Response:

```json
If the request was successful

{
    "sresp": "string",
    "status": 1,
    "meta": {
        "path": "string",
        "id": 0,
        "filename": "string"
    }
}
```

`POST {{url}}/documents`

## View File

Get File by file_path

> Request:

```shell
curl -X GET \
  {{url}}/documents?file_path={{file_path}} \
  -H "Content-type: application/json"  \
  -H 'Authorization: YOUR_TOKEN' \
```

`GET {{url}}/documents?file_path={{file_path}}`

## Sanction Docs

Get sanction docs by app_id

> Request:

```shell
curl -X POST \
  {{url}}/documents/sanction \
  -H "Content-type: application/json"  \
  -H 'Authorization: YOUR_TOKEN' \
  -d '{
    "app_id": "string"
  }'
```

> Response:

```json
If the request was successful

{
  "sanction_letter": "string",
  "nach_mandate": "string",
  "lss": "string",
  "loan_agreement": "string"
}

Error responses
-
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

`POST {{url}}/documents/sanction`
