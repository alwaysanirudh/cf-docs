# Disbursal
Use these set of API's for tranche related actions for PayLater profiles only.

<aside>
	These are not applicable for loan types such as UBL, MCA and Consumer
</aside>

## Block Amount
Blocking an amount is similar to adding an item into your check out cart. Using this API, you can block an amount on the line of the borrower. This will reduce the available limit of the borrower

```shell
Request:
/cf/paylater/block
{
"orderID" : "string",
"amount": "3748973.97"
}
```

```shell
Response :
(success)
{
"status": 1,
"orderID" : "string",
"message": ""
}
//use the orderID in this response to create tranche from this block
(fail)
{
"status": -1,
"message": ""
}
```

## OTP Confirmation on a block

When a request to create a block is triggered, an OTP is sent to the borrower's registered email and phone number for verification

**Verify OTP at block level**

```shell
Request:
/cf/paylater/verify_block_otp
RequestBody:
{
"orderID" : "13",
"otp":"1234"
}
```

```shell
Respone:
{'status': 1, 'message': 'Success'}
Error status codes :
{"status": -9, "message" :"OTP not matching"}
{"status": -13, "message" :"Block not found"}
```

**Resend OTP**

```shell
Request:
/cf/paylater/resend_block_otp
RequestBody :
{
"orderID" : "13"
}
```

```shell
Response:
{"status": "1", "message": "Sent OTP successfully"}
```

## Create Tranche

```shell
Request:
/cf/paylater/createtranchevendor
{
"amount": "88558",
"orderID": "string",
"suborderID": "string"
}
```

```shell
Response:
(success)
{
"status": 1,
"trancheID": "string",
"message": ""
}
//Use this trancheID for reference to this tranche
(fail)
{
"status": -1,
"message": ""
}
```

## Remove Block Amount

```shell
Request:
/cf/paylater/cancel
{
"orderID": "string",
"amount": "3748973.97"
}
```

```shell
Response :
(success)
{
"status": 1,
"message": ""
}
(fail)
{
"status": -1,
"message": ""
}
```

## Fetch Block Balance

```shell
Request:
/cf/paylater/bal
{
"orderID": "string"
}
```

```shell
Response :
{
"status": 1,
"orderID": "string",
"balance": ""
}
```

## Fetch Borrower Details

```shell
URL:
/cf/paylater/agent_info

Request:

{
"email": "testcapitalfloat@gmail.com"
}
```

```shell
Response:
{
"sresp": {
"overdueFees": 0,
"amountNotPaidAfterDueDate": 0,
"otpNotVerified": 0,
"agentProfiles": [
{
"emailId": "testcapitalfloat@gmail.com",
"roi": 13,
"settledAmountTillDate": 0,
"settledTranches": [],
"delayedTranches": [
{
"emailId": "testcapitalfloat@gmail.com",
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
"thumbnailURL": "https://docs-generic.s3-us-west-2.amazonaws.com/testcapitalfloatgmailcom/paylater/d016bad6-527e-484a-b069-afb23563779d/cce5f578-d7d8-4b80-939a-9f50a5f29061/1499879473493_thumbnail.jpg"
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