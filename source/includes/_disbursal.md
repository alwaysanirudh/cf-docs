# Disbursal

## Block Amount

> Request:

```shell
curl -X POST \
  {{url}}/paylater/block \
  -H "Content-type: application/json"  \
  -H 'Authorization: YOUR_TOKEN' \
  -d '{
    "orderID" : "string",
    "amount": "3748973.97"
  }'
```

> Response:

```json
# Success

{
  "status": 1,
  "orderID": "string",
  "message": ""
}

# use the orderID in this response to create tranche from this block

# Fail

{
  "status": -1,
  "message": ""
}
```

`POST {{url}}/paylater/block`

## OTP Confirmation

When a request to create a block is triggered, the otp is being sent via sms and email .

### Verify Block OTP

> Request:

```shell
curl -X POST \
  {{url}}/paylater/verify_block_otp \
  -H "Content-type: application/json"  \
  -H 'Authorization: YOUR_TOKEN' \
  -d '{
    "orderID" : "13",
    "otp":"1234"
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
  "status": -9,
  "message": "OTP not matching"
}
{
  "status": -13,
  "message" :"Block not found"
}
```

`POST {{url}}/paylater/verify_block_otp`

### Resend OTP

> Request:

```shell
curl -X POST \
  {{url}}/paylater/resend_block_otp \
  -H "Content-type: application/json"  \
  -H 'Authorization: YOUR_TOKEN' \
  -d '{
    "orderID" : "13"
  }'
```

> Response:

```json
# On Success

{
  "status": "1",
  "message": "Sent OTP successfully"
}
```

`POST {{url}}/paylater/resend_block_otp`

## Create Tranche

> Request:

```shell
curl -X POST \
  {{url}}/paylater/createtranchevendor \
  -H "Content-type: application/json"  \
  -H 'Authorization: YOUR_TOKEN' \
  -d '{
    "amount": "88558",
    "orderID": "string",
    "suborderID": "string"
  }'
```

> Response:

```json
# Success
{
"status": 1,
"trancheID": "string",
"message": ""
}
# Use this trancheID for reference to this tranche

# Failure
{
"status": -1,
"message": ""
}
```

`POST {{url}}/paylater/createtranchevendor`

## Remove Block Amount

> Request:

```shell
curl -X POST \
  {{url}}/paylater/cancel \
  -H "Content-type: application/json"  \
  -H 'Authorization: YOUR_TOKEN' \
  -d '{
    "orderID": "string",
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
"status": -1,
"message": ""
}
```

`POST {{url}}/paylater/cancel`

## Fetch Block Balance

> Request:

```shell
curl -X POST \
  {{url}}/paylater/bal \
  -H "Content-type: application/json"  \
  -H 'Authorization: YOUR_TOKEN' \
  -d '{
    "orderID": "string"
  }'
```

> Response :

```json
{
  "status": 1,
  "orderID": "string",
  "balance": ""
}
```

`POST {{url}}/paylater/bal`

## Fetch Borrower Details

> Request:

```shell
curl -X POST \
  {{url}}/paylater/agent_info \
  -H "Content-type: application/json"  \
  -H 'Authorization: YOUR_TOKEN' \
  -d '{
    "email": "testcapitalfloat@gmail.com"
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
        "emailId": "t.e.s.t.c.a.p.i.t.a.l.f.l.o.a.t@gmail.com",
        "roi": 13,
        "settledAmountTillDate": 0,
        "settledTranches": [],
        "delayedTranches": [
          {
            "emailId": "t.e.s.t.c.a.p.i.t.a.l.f.l.o.a.t@gmail.com",
            "totalDelinquentAmount": "145152.862215278",
            "trancheId": "cce5f578-d7d8-4b80-939a-9f50a5f29061",
            "dpd": 25,
            "payments": [],
            "dueAmt": {
              "charges": 3636.189999999973,
              "total": 145152.8622152778,
              "interest": 1516.67,
              "principal": 140000
            },
            "totalFeesDue": 0,
            "agentId": null,
            "invoiceUrls": [
              {
                "caption": "1234",
                "thumbnailURL":
                  "https://docs-generic.s3-us-west-2.amazonaws.com/testcapitalfloatgmailcom/paylater/d016bad6-527e-484a-b069-afb23563779d/cce5f578-d7d8-4b80-939a-9f50a5f29061/1499879473493_thumbnail.jpg"
              }
            ],
            "dueDate": "8/12/2017 12:00:00 AM"
          }
        ],
        "sanctionId": "d016bad6-527e-484a-b069-afb23563779d",
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
        "lan": "BAN17E00575",
        "amountNotPaidAfterDueDate": 145152.8622152778,
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
        "overdueCharges": 3636.189999999973,
        "dueTranches": []
      }
    ],
    "pendingTranchesForFunding": 0,
    "agent": {
      "city": null,
      "name": "Deepak Elec Pvt Ltd",
      "country": null,
      "phone": null,
      "agent_id": null,
      "email": null
    },
    "settledAmountTillDate": 145152.8622152778,
    "dpd": 25,
    "cfBankIfsc": "RATN0000156",
    "overduePrincipal": 140000,
    "overdueCharges": 3636.189999999973,
    "overdueInterest": 1516.67,
    "cfBankAcctNo": "VACAFLT08483",
    "cfBankName": "RBL"
  },
  "status": 1
}
```

`POST {{url}}/paylater/agent_info`
