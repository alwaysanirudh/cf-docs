# Application Flow

## Application Status

> Request:

```shell
curl -X POST \
  {{url}}/applications/status\
  -H "Content-type: application/json"  \
  -H 'Authorization: YOUR_TOKEN' \
  -d '{
    "app_id": "string"
  }'
```

> Response :

```json
# Success

If the application if approved with Offer
{
  "status": 200,
  "app_status": "string",
  "app_status_label": "string",
  "app_id": "string",
  "sub_type": "string",
  "is_active": "0|1",
  "suspend_reason": "string",
  "offer": {
    "minDocFee": "string",
    "maxDocFee": "string",
    "maxRoi": "string",
    "minRoi": "string",
    "pfAmount": "string",
    "productTrack": "string",
    "loanProdType": "string",
    "loanAmount": "string",
    "emi": "string",
    "daysPerCycle": "string",
    "isReducing": "0|1",
    "sanctionedPf": "string",
    "tenure": "string"
  }
}

If the application is rejected. The reject reason will be provide whenever necessary
{
  "status": 200,
  "app_status": "string",
  "app_id": "string",
  "reject_reason": "string"
}

# Failure
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
  "message": "App not found"
}
{
  "status": -400,
  "message": "Not authorized to view this app"
}
{
  "status": -500,
  "message":"Failure in fetching sanction status"
}
```

`POST {{url}}/applications/status`

**Possible app status**

| app_status | app_status_label     |
| ---------- | -------------------- |
| 200        | App in progress      |
| 300        | App Submitted        |
| 400        | App Verified         |
| 450        | COH Decision Pending |
| 500        | Request for login    |
| 600        | File logged-in       |
| 700        | Cam in Progress      |
| 800        | Cam Completed        |
| 900        | Pd in Progress       |
| 1000       | Pd Completed         |
| 1100       | Approved             |
| 1200       | Rejected             |
| 10000      | Disbursed            |
| 11000      | KYC Done             |
| 12000      | CIBIL Pulled         |
| 14000      | Loan Agreement Done  |
| 15000      | NACH Done            |
| 16000      | DOC UPLOAD Done      |
| 20000      | Customer Acceptance  |

**Possible profile suspension reason**

| suspend_reason                       |
| ------------------------------------ |
| Due to delinquency / RTR (temporary) |
| Due to delinquency / RTR (permanent) |
| Customer Requested                   |
| Deprecated                           |
| Line Expired                         |
| Potential Fraud                      |
| Confirmed Fraud                      |
| Sold                                 |
| Partner Requested                    |
| Delinquent on other CF loan          |
| Closed by collections                |
| Partnership Shutdown                 |
| Profile fees are due                 |

**Loan offer Parameters**

| Name          | Type   | Description            |
| ------------- | ------ | ---------------------- |
| sanctionedRoi | string | Rate of interest       |
| minDocFee     | string | Minimum Doc Fee        |
| maxDocFee     | string | Maximum Doc Fee        |
| pfAmount      | string | Processing Fee         |
| productTrack  | string | Product track          |
| loanProdType  | string | Loan Type              |
| loanAmount    | string | Loan amount            |
| emi           | string | EMI                    |
| daysPerCycle  | string | Days per Cycle         |
| isReducing    | string | Interest type reducing |
| sanctionedPf  | string | Processing Fee %       |
| tenure        | string | Loan Tenure            |

## Bank Details

This API can be used to Repayment/Disbursal bank account for the loan application.

> Request:

```shell
curl -X POST \
  {{url}}/applications/bank_details\
  -H "Content-type: application/json"  \
  -H 'Authorization: YOUR_TOKEN' \
  -d '{
    "app_id": "string",
    "code": "string"
    "accountNumber": "string"
    "bankName": "string"
    "branchName": "string"
    "accountHolderName": "string"
    "verified": "string",
    "city": "string"
    "isBankLinkedToAadhaar": "string"
    "accountType": "string"
    "modeOfOperation": "string"
  }'
```

> Response :

```json
# Success
{
  "status": 200
}

# Failure
{
  "status": 400
}
```

`POST {{url}}/applications/bank_details`

## Application Tasks

> Request:

```shell
curl -X POST \
  {{url}}/applications/{{task}}\
  -H "Content-type: application/json"  \
  -H 'Authorization: YOUR_TOKEN' \
  -d '{
    "app_id": "string"
  }'
```

> Response :

```json
# Success

If task is marked as done
{
  "status": 200,
  "message": "Task Updated"
}

# Failure
{
  "status": -100,
  "message": "Payload is missing app_id"
}
{
  "status": -200,
  "message": "App not found"
}
{
  "status": -300,
  "message": "Not authorized to view this app"
}
{
  "status": -400,
  "message":"Task Update Failed"
}
```

`POST {{url}}/applications/{{task}}`

| task                |
| ------------------- |
| customer_acceptance |
| login_request       |

## Application Callbacks

Once an app_id is created. CF will post to your configured Callbacks on registered events.
For now configuration of Callbacks and registration of events is offline. Share these details with CF representative you are in touch with.
For details please refer [application-status](#application-status)

`eg: {{your_domain}}/capitalfloat/callback`

> Request:

```json
{
  "status": 200,
  "app_status": "string",
  "app_status_label": "string",
  "app_id": "string",
  "sub_type": "string",
  "is_active": "0|1",
  "suspend_reason": "string",
  "offer": {
    "sanctionedRoi": "string",
    "minDocFee": "string",
    "maxDocFee": "string",
    "pfAmount": "string",
    "productTrack": "string",
    "loanProdType": "string",
    "loanAmount": "string",
    "emi": "string",
    "daysPerCycle": "string",
    "isReducing": "0|1",
    "sanctionedPf": "string",
    "tenure": "string"
  }
}


# Callback on repayment
{
  "status": 200,
  "app_status": 10000,
  "app_status_label": "Disbursed",
  "app_id": "string",
  "repayment": {
     "merchantId": "string",
     "merchantName": "string",
     "amountPaid": 0,
     "chargesPaid": 0,
     "interestPaid": 0,
     "principalPaid": 0,
     "feesPaid": 0,
     "creditAccountBalance": 0,
     "amountDue": 0,
     "shortfall": 0,
     "mode": "string",
     "refNum1": "string",
     "refNum2": "string",
     "refNum3": "string"
  }
}
```

**Possible modes**

| mode   |
| ------ |
| Cash   |
| NEFT   |
| RTGS   |
| IMPS   |
| IFT    |
| UPI    |
| PDC    |
| NACH   |
| Cheque |
| AEPS   |
| DD     |
| DDM    |
| ENACH  |