# Disbursal

## Block Amount

> Request:

```shell
curl -X POST \
  {{url}}/paylater/block \
  -H "Content-type: application/json"  \
  -H 'Authorization: YOUR_TOKEN' \
  -d '{
    "app_id": "string",
    "order_id" : "string",
    "amount": "3748973.97"
  }'
```

> Response:

```json
# Success

{
  "status": 1,
  "order_id": "string",
  "message": "string"
}

# use the order_id in this response to create tranche from this block

# Error status codes
{
    "status": -100,
    "message": "Payload is missing amount or app_id or order_id"
}
{
    "status": -200,
    "message": "No partner found for current user"
}
{
    "status": -300,
    "message": "Amount cannot be negative. Please provide a proper value"
}
{
    "status": -400,
    "message": "App not found"
}
{
    "status": -500,
    "message": "Not authorized to view this app"
}
{
    "status": -600,
    "message": "Borrower not found"
}
{
    "status": -700,
    "message": "Vendor not found"
}
{
    "status": -800,
    "message": "Sanction not found"
}
{
    "status": -900,
    "message": "Tranche creation has been suspended for the borrower. Please consult Capital Float"
}
{
    "status": -1000,
    "message": "The request could not be processed. Please consult Capital Float"
}
```

`POST {{url}}/paylater/block`

## OTP Confirmation

When a request to create a block is triggered, the otp is being sent via sms and email .

### Verify Block OTP

> Request:

```shell
curl -X POST \
  {{url}}/paylater/verify_block \
  -H "Content-type: application/json"  \
  -H 'Authorization: YOUR_TOKEN' \
  -d '{
    "app_id": "string",
    "order_id" : "string",
    "otp":"string"
  }'
```

> Response:

```json
# On Success:
{
  "status": 1,
  "message": "Success"
}

# Error status codes :
{
  "status": -100,
  "message": "Payload is missing amount or app_id or order_id"
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
  "message" :"Sanction not found for the app"
}
```

`POST {{url}}/paylater/verify_block`

### Resend OTP

> Request:

```shell
curl -X POST \
  {{url}}/paylater/resend_block_otp \
  -H "Content-type: application/json"  \
  -H 'Authorization: YOUR_TOKEN' \
  -d '{
    "app_id": "string"
    "order_id" : "13"
  }'
```

> Response:

```json
# On Success

{
  "status": "1",
  "message": "OTP sent successfully"
}

# Error status codes :
{
  "status": -100,
  "message": "Payload is missing app_id or order_id"
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
  "message" :"Borrower not found"
}
{
  "status": -600,
  "message" :"Sanction not found"
}
```

`POST {{url}}/paylater/resend_block_otp`

## Create Tranche

> Request:

```shell
curl -X POST \
  {{url}}/paylater/tranche \
  -H "Content-type: application/json"  \
  -H 'Authorization: YOUR_TOKEN' \
  -d '{
    "app_id": "string"
    "amount": "string",
    "order_id": "string",
    "suborder_id": "string"
  }'
```

> Response:

```json
# Success
{
"status": 1,
"tranche_id": "string",
"message": ""
}
# Use this trancheID for reference to this tranche

# Failure
{
  "status": -100,
  "message": "Payload is missing amount or app_id or order_id"
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
  "message" :"Borrower not found"
}
{
  "status": -600,
  "message" :"Vendor not found"
}
{
  "status": -700,
  "message" :"Sanction not found"
}
{
  "status": -900,
  "message" :"The request could not be processed. Please consult Capital Float"
}
{
  "status": -1000,
  "message" :"Bank not found"
}
{
  "status": -1100,
  "message" :"Vendor bank details not found"
}
{
  "status": -1200,
  "message" :"The request could not be processed. Please consult Capital Float"
}
{
  "status": -1300,
  "message" :"The request could not be processed. Please consult Capital Float"
}
```

`POST {{url}}/paylater/tranche`

## Remove Block Amount

> Request:

```shell
curl -X POST \
  {{url}}/paylater/cancel \
  -H "Content-type: application/json"  \
  -H 'Authorization: YOUR_TOKEN' \
  -d '{
    "app_id": "string",
    "order_id": "string",
    "amount": "3748973.97"
  }'
```

> Response:

```json
# Success
{
  "status": 1,
  "message": ""
}
# Failure
{
  "status": -100,
  "message": "Payload is missing amount or app_id or order_id"
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
{
  "status": -600,
  "message" :"Borrower not found"
}
{
  "status": -700,
  "message" :"Vendor not found"
}
{
  "status": -800,
  "message" :"Vendor config not found"
}
{
  "status": -900,
  "message" :"The request could not be processed. Please consult Capital Float"
}
```

`POST {{url}}/paylater/cancel`

## Fetch Block Balance

> Request:

```shell
curl -X POST \
  {{url}}/paylater/balance \
  -H "Content-type: application/json"  \
  -H 'Authorization: YOUR_TOKEN' \
  -d '{
    "app_id": "string",
    "order_id": "string"
  }'
```

> Response :

```json
# Success
{
  "status": 1,
  "order_id": "string",
  "balance": ""
}

# Failure
{
  "status": -100,
  "message": "Payload is missing app_id or order_id"
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
{
  "status": -600,
  "message" :"Vendor not found"
}
{
  "status": -700,
  "message" :"The request could not be processed. Please consult Capital Float"
}
```

`POST {{url}}/paylater/balance`

## Fetch Borrower Details

> Request:

```shell
curl -X POST \
  {{url}}/paylater/agent_info \
  -H "Content-type: application/json"  \
  -H 'Authorization: YOUR_TOKEN' \
  -d '{
    "app_id": "string"
  }'
```

> Response:

```json
{
  "sresp": {
    "overdueFees": 0,
    "amountNotPaidAfterDueDate": 0,
    "otpNotVerified": 0,
    "agentProfiles": [
      {
        "emailId": "abc@xyz.com",
        "roi": 13,
        "settledAmountTillDate": 0,
        "settledTranches": [],
        "delayedTranches": [
          {
            "emailId": "abc@xyz.com",
            "totalDelinquentAmount": "145152.86",
            "trancheId": "bbe5f578-d7d8-4b80-939a-9f50a5f29061",
            "dpd": 25,
            "payments": [],
            "dueAmt": {
              "charges": 3636.18,
              "total": 145152.86,
              "interest": 1516.67,
              "principal": 140000
            },
            "totalFeesDue": 0,
            "agentId": null,
            "invoiceUrls": [
              {
                "caption": "1234",
                "thumbnailURL": "SOME_URL"
              }
            ],
            "dueDate": "8/12/2017 12:00:00 AM"
          }
        ],
        "sanctionId": "e116bad6-527e-484a-b069-afb23563779d",
        "requestedTranches": [],
        "pendingTranchesForFunding": 0,
        "penaltyInterestPa": "37.0",
        "nachStatus": "Rejected",
        "dueDateOfNextTranche": null,
        "expiryDate": "2018-10-05",
        "expectedIr": "13",
        "totalLimitUtilized": 140000,
        "isOnHold": "Active",
        "overdueFees": 0,
        "lan": "AAA17E00000",
        "amountNotPaidAfterDueDate": 145152.86,
        "otpNotVerified": 0,
        "availableLimit": 716543,
        "creditLimit": 876543,
        "overdueInterest": 1516.67,
        "creationDate": "2017-07-12",
        "repaymentCycle": 30,
        "isActive": true,
        "activeBlockedAmount": 10000,
        "overduePrincipal": 140000,
        "dpd": 25,
        "onHoldReason": "-",
        "overdueCharges": 3636.18,
        "dueTranches": []
      }
    ],
    "pendingTranchesForFunding": 0,
    "agent": {
      "city": null,
      "name": "Abc Pvt Ltd",
      "country": null,
      "phone": null,
      "agent_id": null,
      "email": null
    },
    "settledAmountTillDate": 145152.86,
    "dpd": 25,
    "cfBankIfsc": "RATN0000156",
    "overduePrincipal": 140000,
    "overdueCharges": 3636.18,
    "overdueInterest": 1516.67,
    "cfBankAcctNo": "VACAFLT00000",
    "cfBankName": "RBL"
  },
  "status": 1
}
```

`POST {{url}}/paylater/agent_info`

## Fetch Profile Available Limit

> Request:

```shell
curl -X POST \
  {{url}}/paylater/profile_available_limit \
  -H "Content-type: application/json"  \
  -H 'Authorization: YOUR_TOKEN' \
  -d '{
    "app_id": "string"
  }'
```

> Response :

```json
# Success
{
  "status": 1,
  "available_limit": "string",
  "app_id": "string"
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
{
  "status": -600,
  "message" :"Vendor not found"
}
{
  "status": -700,
  "app_id": "string",
  "message" :"The request could not be processed. Please consult Capital Float"
}
```

`POST {{url}}/paylater/profile_available_limit`

## Common Error codes

> Response:

```json
# Common error codes (message text might change but meaning remains same)

{
    "status": -1,
    "message": "sanction with sanctionID 'string' doesn't exist"
}
{
    "status": -2,
    "message": "invalid loan type"
}
{
    "status": -3,
    "message": "sanction credit limit is exceeding"
}
{
    "status": -4,
    "message": "sanction credit limit is empty"
}
{
    "status": -5,
    "message": "number format exception"
}
{
    "status": -6,
    "message": "tranche amount is not integer"
}
{
    "status": -7,
    "message": "tranche limit is null"
}
{
    "status": -8,
    "message": "lms limit is empty"
}
{
    "status": -9,
    "message": "tranche amount exceeding lms limit"
}
{
    "status": -10,
    "message": "unable to create tranche"
}
{
    "status": -11,
    "message": "bad json"
}
{
    "status": -12,
    "message": "blocked order not found"
}
{
    "status": -13,
    "message": "duplicate blocked order"
}
{
    "status": -14,
    "message": "tranche not found"
}
{
    "status": -15,
    "message": "tranche not open to all"
}
{
    "status": -16,
    "message": "investor already exists"
}
{
    "status": -17,
    "message": "investor not found"
}
{
    "status": -18,
    "message": "investor amount roi invalid"
}
{
    "status": -19,
    "message": "investor portal not found"
}
{
    "status": -20,
    "message": "scheduled disbursal not set"
}
{
    "status": -21,
    "message": "disbursal schedule date not set"
}
{
    "status": -22,
    "message": "disbursal schedule date is in past"
}
{
    "status": -23,
    "message": "otp not verified"
}
{
    "status": -24,
    "message": "amount not blocked"
}
{
    "status": -25,
    "message": "amount not unblocked"
}
```
