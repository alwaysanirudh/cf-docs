# Repayment

Using these API's, you can check the upcoming payments

## Repayment Info

> Request:

```shell
curl -X POST \
  {{url}}/application/repayment_info \
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
    "amountDue": 0,
    "amountDueOnDueDate": 0,
    "amountPaid": 0,
    "amountTransferred": 0,
    "annualInterestRate": "string",
    "appId": "string",
    "cfAccountName": "string",
    "cfBankAcctNo": "string",
    "cfBankIfsc": "string",
    "cfBankName": "string",
    "chargesDue": 0,
    "chargesDueOnDueDate": 0,
    "chargesPaid": 0,
    "chequeBounceCount": 0,
    "creditAcctBalance": 0,
    "daysPerCycle": "string",
    "debitDate": "string",
    "disbursedAmount": 0,
    "dpd": 0,
    "dueDate": "string",
    "emiAmount": "string",
    "feesDue": 0,
    "feesPaid": 0,
    "interestDue": 0,
    "interestDueOnDueDate": 0,
    "interestPaid": 0,
    "nameOfBusiness": "string",
    "penaltyInterestRate": "string",
    "principalDue": 0,
    "principalPaid": 0,
    "principleDueOnDueDate": 0,
    "repaymentMode": "string",
    "repaymentModeRegistrationStatus": "string",
    "shortfall": 0
  },
  "status": 1
}
```

This API provides repayment info by app_id.

`POST {{url}}/application/repayment_info`
