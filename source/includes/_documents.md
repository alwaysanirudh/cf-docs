# Documents

## Fetch files

Fetch files uploaded for an application.
NOTE: If documents for a application were never uploaded; this API needs to be called first. It will create the document sections if they are not created.

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

`GET {{url}}/documents/files?appid={{appid}}`

## Document List

View document list for an application. This also returns the files in each doc section if they were uploaded.

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
    "Company KYC": {
        "Co:ownership_proof": [],
        "Co:Recent Utility/Landline bill": [
        ],
        "co:vintage": [],
        "Co:Partnership Deed": [],
        "Co:PAN Copy": []
    },
    "Ops Documents": {
        "EXTRA_DOCS:app_address_osv_pr_osv_384852": [],
        "EXTRA_DOCS:sancton_letter_section": [],
        "EXTRA_DOCS:NACH_mandate": [],
        "EXTRA_DOCS:app_address_osv_pr_osv_384851": [],
        "EXTRA_DOCS:company_address_proof_osv": [],
        "EXTRA_DOCS:app_id_osv_pr_osv_384852": [],
        "EXTRA_DOCS:app_id_osv_pr_osv_384851": [],
        "EXTRA_DOCS:company_pan_osv": [],
        "EXTRA_DOCS:pdc": [],
        "EXTRA_DOCS:loan_agreement": []
    },
    "Company Financials": {
        "Co:VAT/ST Returns (Apr'13-Current)": [],
        "Co:Last 12 months Bank Stmts": [],
        "Co:Current loans-Sanction letters": []
    },
    "Promoter KYC": {
        "Pr:ownership_proof_pr_384852": [],
        "Pr:ownership_proof_pr_384851": [],
        "Pr:Utility/Mobile Bills_pr_384851": [],
        "Pr:Utility/Mobile Bills_pr_384852": [],
        "Pr:PAN Copies_pr_384851": [
            {
                "path_name": "f7a77e35-82f0-442c-bf20-8ce9b681af98/1c6977bf-9857-45f5-9a0b-a5314894220c.png",
                "extra_tag_name": "",
                "ts": "2018-04-25 07:28:52",
                "tags": "Pr:PAN Copies_pr_384851",
                "synced": 0,
                "extra_tag_id": 0,
                "size": null,
                "id": 1597546,
                "filename": "Pan.png"
            }
        ],
        "Pr:PAN Copies_pr_384852": []
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
  -F 'file=@/filepath/pan.png' \
  -F 'password=pass1234'
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

View an uploaded file

> Request:

```shell
curl -X GET \
  {{url}}/documents?file_path={{file_path}} \
  -H "Content-type: application/json"  \
  -H 'Authorization: YOUR_TOKEN' \
```

`GET {{url}}/documents?file_path={{file_path}}`

## Sanction Docs

Get sanction docs of an application

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
