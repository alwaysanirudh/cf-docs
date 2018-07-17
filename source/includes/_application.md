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
  "is_active": "0|1",
  "suspend_reason": "string",
  "resume_reason": "string",
  "offer": {
    "minDocFee": "string",
    "maxDocFee": "string",
    "maxRoi": "string",
    "minRoi": "string",
    "minPf": "string",
    "maxPf": "string",
    "finalPfAmt": "string",
    "minTransactionFee": "string",
    "maxTransactionFee": "string",
    "withHoldingAmt": "string",
    "withHoldingPc": "string",
    "productTrack": "string",
    "loanProdType": "string",
    "loanAmt": "string",
    "emi": "string",
    "daysPerCycle": "string",
    "isReducing": "0|1",
    "tenure": "string",
    "noOfCycles": "string"
  },
  "push_forward": [
    {
      "files": [
        {
          "path": "string",
          "filename": "string"
        }
      ],
      "status": 0,
      "is_extra": false,
      "tag": "string",
      "description": "string",
      "id": 0,
      "comments": [
          "string"
      ]
    }
  ],
  "event": "string"
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
  "message": "Failure in fetching sanction status"
}
{
  "status": -600,
  "message": "Request could not be processed"
}
```

`POST {{url}}/applications/status`

**Notes:**

* `event` key will be present only when documents have been pushed forward or customer consent request has been raised

* `push_forward` key will be present only when the value of event key is `push_forward`

* `is_active`, `resume_reason` and `suspend_reason` keys will be present only if the sanction has been disbursed

* `offer` key will be present if sanction is dibsursed or the app status is 'App Verified' or 'Approved'

* **Please note that the status api will not have data of events like Repayment and Sanction Docs Generated**


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

| Name              | Type   | Description              |
| ----------------- | ------ | ------------------------ |
| minRoi            | string | Minimum Rate of interest |
| maxRoi            | string | Maximum Rate of interest |
| minTransactionFee | string | Minimum Transaction Fee  |
| maxTransactionFee | string | Maximum Transaction Fee  |
| minDocFee         | string | Minimum Doc Fee          |
| maxDocFee         | string | Maximum Doc Fee          |
| finalDocFeeAmt    | string | Final Doc Fee            |
| minPf             | string | Minimum Processing Fee % |
| maxPf             | string | Maximum Processing Fee % |
| finalPfAmt        | string | Final Process Fee Amount |
| finalPremiumAmt   | string | Final Premium Amount     |
| loanProdType      | string | Loan Type                |
| loanAmt           | string | Loan amount              |
| emi               | string | EMI                      |
| daysPerCycle      | string | Days per Cycle           |
| noOfCycles        | string | No. of Cycles            |
| isReducing        | string | Interest type reducing   |
| tenure            | string | Loan Tenure              |
| withHoldingAmt    | string | Withholding Amount       |
| withHoldingPc     | string | Withholding %            |

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
    "code": "string",
    "accountNumber": "string",
    "bankName": "string",
    "branchName": "string",
    "accountHolderName": "string",
    "verified": "string",
    "city": "string",
    "isBankLinkedToAadhaar": "string",
    "accountType": "string",
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
for task - customer_acceptance, login_request, sanction_docs
{
  "status": 200,
  "message": "Task Updated"
}

for task - push_back
{
  "status": 200,
  "message": "Push back successful"
}

# Failure
Common error codes
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
  "message": "Task Update Failed"
}
{
  "status": -500,
  "message": "Invalid Operation"
}

for task - login_request
{
  "status": -600,
  "message" :"Login Request Failed"
}

for task - push_back
{
  "status": -600,
  "message" :"Unable to verify docs"
}
{
  "status": -700,
  "message" :"Unable to do push back"
}

for task - sanction_docs
{
  "status": -600,
  "message" :"Please verify all sections or mark an exception where required before submitting to Ops !"
}
```

`POST {{url}}/applications/{{task}}`

| task                |
| ------------------- |
| login_request       |
| push_back           |
| customer_acceptance |
| sanction_docs       |

## Application Callbacks

Once an app_id is created. CF will post to your configured Callbacks on registered events.
For now configuration of Callbacks and registration of events is offline. Share these details with CF representative you are in touch with.
For details please refer [application-status](#application-status)

`eg: {{your_domain}}/{{your_endpoint}}`

### App Verified

* This callback is posted after auto app verification
* This has the loan amount calculated after running the DE policy

```json
# App Verified
{
  "status": 200,
  "app_status": 400,
  "app_status_label": "string",
  "app_id": "string",
  "offer": {
    "loanAmt": "string"
  }
}
```

### Push Forward

* The documents where action needs to be taken will be posted here
* Possible doc status

    | status | label      |
    | ------ | ---------- |
    | 0      | QC Pending |
    | 1      | QC Accept  |
    | 2      | QC Reject  |

```json
{
  "app_status": 500,
  "app_status_label": "Request for login",
  "event": "push_forward",
  "status": 200,
  "app_id": "string",
  "push_forward": [
    {
      "files": [
        {
          "path": "string",
          "filename": "string"
        }
      ],
      "status": 0,
      "is_extra": false,
      "tag": "string",
      "description": "string",
      "id": 0,
      "comments": [
          "string"
      ]
    }
  ]
}
```

### File Login, PD, CAM

* These events are identified by the app status

```json
{
  "status": 200,
  "app_status": 0,
  "app_status_label": "string",
  "app_id": "string"
}
```

### Customer Consent
* Latest loan offer from sales is sent in this callback when the customer consent event is triggered

```json
{
  "status": 200,
  "app_status": 0,
  "app_status_label": "string",
  "event": "customer_consent",
  "app_id": "string",
  "offer": {
    "tenure": "string",
    "loanAmt": "string",
    "minEmi": "string",
    "maxEmi": "string",
    "tenure": "string",
    "daysPerCycle": "string",
    "noOfCycles": "string",
    "minPf": "string",
    "maxPf": "string",
    "minTransactionFee": "string",
    "minDocFee": "string",
    "maxDocFee": "string",
    "minRoi": "string",
    "maxRoi": "string",
    "withHoldingAmt": "string",
    "withHoldingPc": "string",
    "isReducing": 0,
    "loanProdType": "string"
  }
}
```

### Sanction docs
* Generated sanction docs are sent in this callback, it is triggered after the investors in a sanction are finalized

```json
{
  "status": 200,
  "app_status": 0,
  "app_status_label": "string",
  "event": "sanction_docs",
  "app_id": "string",
  "offer": {
    "tenure": "string",
    "loanAmt": "string",
    "minEmi": "string",
    "maxEmi": "string",
    "tenure": "string",
    "daysPerCycle": "string",
    "noOfCycles": "string",
    "minPf": "string",
    "maxPf": "string",
    "minTransactionFee": "string",
    "minDocFee": "string",
    "maxDocFee": "string",
    "minRoi": "string",
    "maxRoi": "string",
    "withHoldingAmt": "string",
    "withHoldingPc": "string",
    "isReducing": 0,
    "loanProdType": "string"
  },
  "sanction_docs": {
    "sanction_letter": "string",
    "nach_mandate": "string",
    "lss": "string",
    "loan_agreement": "string"
  },
}
```

### Disbursal
* On disbursal the callback will have the final loan offer values and the sanction status

```json
{
  "status": 200,
  "app_status": 0,
  "app_status_label": "string",
  "app_id": "string",
  "is_active": 0,
  "suspend_reason": "string",
  "resume_reason": "string",
  "offer": {
    "tenure": "string",
    "loanAmt": "string",
    "emi": "string",
    "tenure": "string",
    "daysPerCycle": "string",
    "noOfCycles": "string",
    "finalPfAmt": "string",
    "finalPremiumAmt": "string",
    "finalDocFeeAmt": "string",
    "withHoldingAmt": "string",
    "withHoldingPc": "string",
    "roi": "string",
    "isReducing": 0,
    "loanProdType": "string"
  }
}
```


### Repayment
* When a repayment is applied against a loan in the system this callback will be called, it will have the repayment level splits of principal, interest, charges, fees

* Possible modes in repayment callback

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


```json
{
  "status": 200,
  "app_status": 10000,
  "app_status_label": "Disbursed",
  "app_id": "string",
  "is_active": 1,
  "repayment": {
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


### Rejection
* This callback is triggered when an app is rejected, it has the rejection reason of the app

```json
{
  "status": 200,
  "app_status_label": "Rejected",
  "reject_reason": "string",
  "app_status": 1200,
  "app_id": "string"
}
```
