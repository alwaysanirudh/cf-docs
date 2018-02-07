# Repayment

Using these API's, you can check the status of an upcoming payment

## Repayment Info

> Request:

```shell
curl -X POST \
  {{url}}/vendordashboard/get_repayment_info \
  -H "Content-type: application/json"  \
  -H 'Authorization: YOUR_TOKEN' \
  -d '{
  	"agentEmails": ["testcapitalf.loat@gmail.com"]
  }'
```

> Response:

```json
{
  "sresp": [
    {
      "profiles": [
        {
          "lan": "BAN17R00186",
          "tranches": [
            {
              "interestDue": 8666.67,
              "cfAccountName": "Zen Lefin Private Limited",
              "trancheId": "9a89f142-fe57-471c-a1fc-3a5d4e4a63b8",
              "invoiceNo": "",
              "cycleNumber": "1",
              "amountTransferred": 650000,
              "feesPaid": 0,
              "amountDue": 743561.49,
              "principalDue": 650000,
              "dueDate": "01-07-2017",
              "cfBankName": "RBL",
              "chargesDue": 84894.82,
              "cfBankAcctNo": "VACAFLT07926A",
              "amountDueOnDueDate": 743561.49,
              "chargesPaid": 0,
              "cfBankIfsc": "RATN0000156",
              "amountPaid": 0,
              "feesDue": 0,
              "principalPaid": 0,
              "chequeBounceCount": 0,
              "disbursedAmount": 650000,
              "dpd": 116,
              "interestPaid": 0,
              "debitDate": "01-06-2017"
            }
          ]
        }
      ],
      "agent": {
        "city": "Bangalore",
        "name": "Test Industries Pvt Ltd2017-06-01 16:16:45.399",
        "country": null,
        "phone": "9966553315",
        "agent_id": "None",
        "email": "testcapitalf.loat@gmail.com"
      }
    }
  ],
  "status": 1
}
```

This API provides tranche level details for an agent or for all the agents depending upon the data passed in Request. To receive to response for a specific agent, pass agent e-mail in the request. If no e-mail has been entered, the api will return tranche level details for all the agents.

`POST {{url}}/vendordashboard/get_repayment_info`

## Repayment Reminder

> Request:

```shell
curl -X POST \
  {{url}}/vendordashboard/get_due_date_amount \
  -H "Content-type: application/json"  \
  -H 'Authorization: YOUR_TOKEN' \
  -d '{
    "tranche_id": ""
  }'
```

> Response:

```json
{
  "sresp": [
    {
      "dueAmount": 261768.52,
      "dueDate": "2017-10-15"
    }
  ],
  "status": 1
}
```

Provides outstanding/delinquent amount of the borrower at tranche level.

`POST {{url}}/vendordashboard/get_due_date_amount`
