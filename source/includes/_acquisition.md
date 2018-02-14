# Acquisition via API

## Create User
A user is created on Capital Float's system prior to applying for a loan application

> Request:

```shell
curl -X POST \
  {{url}}/users/create_user \
  -H "Content-type: application/json"  \
  -H 'Authorization: YOUR_TOKEN' \
  -d '{
    "email": "string",
    "phone": "string",
    "username": "string",
    "city": "string"
  }'
```

> Response:

``` json
{
"app_id":"SOME_USER_ID"
}
```

`POST {{url}}/users/create_user`

**Parameters**

| Name     | Type   | Description         |
| -------- | ------ | ------------------- |
| email    | string | User's email        |
| phone    | string | User's phone        |
| username | string | User's username     |
| city     | string | User's current city |

## Create Application
Post user creation, the user can now apply for a loan. The loan application is an exhaustive list which accommodates multiple loan types. Not all fields are required.

> Request:

```shell
curl-X POST \
  {{url}}/apps/details/applications \
  -H "Content-type: application/json"  \
  -H 'Authorization: YOUR_TOKEN' \
  -d '{
    "bank_accounts": [
      {
        "acc_context": 0,
        "acc_holder_name": "string",
        "acc_id": 0,
        "acc_no": "string",
        "acc_type": "string",
        "app_id": "string",
        "bank_name": "string",
        "branch": "string",
        "entry_code": 0,
        "ifsc_code": "string"
      }
    ],
    "business_details": [
      {
        "address_list": [
          {
            "address": "string",
            "address_id": 0,
            "address_owner": "string",
            "address_type": 0,
            "app_id": "string",
            "city": "string",
            "contact_list": [
              {
                "address_id": 0,
                "app_id": "string",
                "contact_context": 0,
                "contact_id": 0,
                "contact_information": "string",
                "contact_type": 0,
                "entity_id": 0,
                "entity_type": 0
              }
            ],
            "country": 0,
            "district": "string",
            "entity_id": 0,
            "entity_type": 0,
            "is_active": 0,
            "is_fi_needed": 0,
            "landmark": "string",
            "latitude": 0,
            "longitude": 0,
            "occupancy_start_date": "2018-02-05",
            "ownership_type": 0,
            "pincode": 0,
            "post_office": "string",
            "state": "string"
          }
        ],
        "app_id": "string",
        "application_context": 0,
        "business_id": 0,
        "business_profile": "string",
        "ca_number": "string",
        "cibil_request_id": "string",
        "contacts_list": [
          {
            "address_id": 0,
            "app_id": "string",
            "contact_context": 0,
            "contact_id": 0,
            "contact_information": "string",
            "contact_type": 0,
            "entity_id": 0,
            "entity_type": 0
          }
        ],
        "incorporation_date": "2018-02-05",
        "industry_type": 0,
        "kyc_status": 0,
        "main_product_category": 0,
        "nature_of_business": 0,
        "operate_as": 0,
        "operation_start_date": "2018-02-05",
        "poi_list": [
          {
            "app_id": "string",
            "created_time": 0,
            "entity_id": 0,
            "entity_type": 0,
            "id_information": "string",
            "id_type": 0,
            "last_modified_time": 0,
            "poi_id": 0
          }
        ],
        "registered_name": "string",
        "services_provided": [
          0
        ]
      }
    ],
    "business_financials": {
      "app_id": "string",
      "auto_loan": 0,
      "base_year": 0,
      "home_loan": 0,
      "id": 0,
      "loan_against_property": 0,
      "monthly_emi_obligations": 0,
      "odcc_limit": 0,
      "outstanding_loan_amount": 0,
      "personal_loan": 0,
      "profit_prev_year": 0,
      "profit_this_year": 0,
      "turnover_prev_year": 0,
      "turnover_this_year": 0,
      "unsecured_loan": 0
    },
    "ecosystem_details": [
      {
        "app_id": "string",
        "branch_code": "string",
        "customer_id": "string",
        "ecosystem_id": 0,
        "ecosystem_xns_list": [
          {
            "app_id": "string",
            "base_month": 0,
            "base_month_minus_1": 0,
            "base_month_minus_10": 0,
            "base_month_minus_11": 0,
            "base_month_minus_12": 0,
            "base_month_minus_2": 0,
            "base_month_minus_3": 0,
            "base_month_minus_4": 0,
            "base_month_minus_5": 0,
            "base_month_minus_6": 0,
            "base_month_minus_7": 0,
            "base_month_minus_8": 0,
            "base_month_minus_9": 0,
            "ecosystem_id": 0,
            "months_of_data": 0,
            "xn_type": 0,
            "xns_id": 0
          }
        ],
        "is_verified": 0,
        "partner_id": 0,
        "partner_name": "string",
        "password": "string",
        "payment_cycle": 0,
        "rating": "string",
        "return_percentage": 0,
        "start_date": "2018-02-05",
        "type": 0,
        "url": "string",
        "username": "string",
        "wallet_number": "string"
      }
    ],
    "fund_use_details": [
      {
        "app_id": "string",
        "end_use_id": 0,
        "estimated_cost": 0,
        "loan_amount_required": 0,
        "service_attributes_jsonb": {
          "array": true,
          "big_decimal": true,
          "big_integer": true,
          "binary": true,
          "boolean": true,
          "container_node": true,
          "double": true,
          "float": true,
          "floating_point_number": true,
          "int": true,
          "integral_number": true,
          "long": true,
          "missing_node": true,
          "node_type": "ARRAY",
          "null": true,
          "number": true,
          "object": true,
          "pojo": true,
          "short": true,
          "textual": true,
          "value_node": true
        },
        "usage_type": 0
      }
    ],
    "individual_details": [
      {
        "address_list": [
          {
            "address": "string",
            "address_id": 0,
            "address_owner": "string",
            "address_type": 0,
            "app_id": "string",
            "city": "string",
            "contact_list": [
              {
                "address_id": 0,
                "app_id": "string",
                "contact_context": 0,
                "contact_id": 0,
                "contact_information": "string",
                "contact_type": 0,
                "entity_id": 0,
                "entity_type": 0
              }
            ],
            "country": 0,
            "district": "string",
            "entity_id": 0,
            "entity_type": 0,
            "is_active": 0,
            "is_fi_needed": 0,
            "landmark": "string",
            "latitude": 0,
            "longitude": 0,
            "occupancy_start_date": "2018-02-05",
            "ownership_type": 0,
            "pincode": 0,
            "post_office": "string",
            "state": "string"
          }
        ],
        "app_id": "string",
        "application_context": 0,
        "birth_date": "2018-02-05",
        "bu_relationship_type": 0,
        "bu_share_percent": 0,
        "business_id": 0,
        "cibil_consent_flag": 0,
        "cibil_consent_mode": 0,
        "cibil_request_id": "string",
        "contacts_list": [
          {
            "address_id": 0,
            "app_id": "string",
            "contact_context": 0,
            "contact_id": 0,
            "contact_information": "string",
            "contact_type": 0,
            "entity_id": 0,
            "entity_type": 0
          }
        ],
        "employer_name": "string",
        "employment_type": 0,
        "father_name": "string",
        "first_name": "string",
        "gender": 0,
        "individual_id": 0,
        "individual_relationship_type": 0,
        "kyc_mode": 0,
        "kyc_status": 0,
        "last_name": "string",
        "marital_status": 0,
        "mother_name": "string",
        "poi_list": [
          {
            "app_id": "string",
            "created_time": 0,
            "entity_id": 0,
            "entity_type": 0,
            "id_information": "string",
            "id_type": 0,
            "last_modified_time": 0,
            "poi_id": 0
          }
        ],
        "qualification": 0,
        "work_ex": 0
      }
    ],
    "loan_offer_output": {
      "status": "string",
      "offer": {}
    },
    "metadata": {
      "app_id": "string",
      "app_request_id": "string",
      "app_source_name": "string",
      "application_lifecycle_id": 0,
      "application_segment": 0,
      "application_type": 0,
      "created_time": 0,
      "fin_calc_year": "2018-02-05",
      "hub_or_spoke": 0,
      "in_process_status": 0,
      "is_archived": 0,
      "is_fs": 0,
      "is_perfios": 0,
      "last_modified_time": 0,
      "misc_jsonb": {},
      "pd_context": 0,
      "pd_type": 0,
      "previous_application_id": "string",
      "product_type": 0,
      "sl_no": 0,
      "source_attributes_jsonb": {},
      "status": 0,
      "tags": [
        0
      ],
      "third_party_reference_id": "string",
      "version": "string"
    },
    "renewal_response": {
      "app_id": {
        "id_new": "string",
        "id_old": "string"
      },
      "business_id_change_list": [
        {
          "id_new": "string",
          "id_old": "string"
        }
      ],
      "individual_id_change_list": [
        {
          "id_new": "string",
          "id_old": "string"
        }
      ]
    },
    "user_pool_details_models": [
      {
        "name": "string",
        "pool_context": 0,
        "pool_id": 0,
        "user_id": 0,
        "user_pool_id": 0,
        "username": "string"
      }
    ]
  }'
```

> Response:

``` json
{
"app_id":"SOME_APP_ID"
}
```


`POST {{url}}/apps/details/applications`

**Application Metadata**

| Name                     | Type    | Description                                                                   |
| ------------------------ | ------- | ----------------------------------------------------------------------------- |
| app_id                   | uuid    | App ID auto generated by Capital Float                                        |
| app_request_id           | string  | The Reference ID at your end for posting the application to Capital Float.    |
| app_source_name          | string  | Source of the application. Refer Master                                       |
| application_lifecycle_id | integer |                                                                               |
| aapplication_segment     | integer | Application Segment (example: Individual/Business). Refer Master.             |
| application_type         | integer | Type of application. Refer Master                                             |
| created_time             | integer | Creation time for application                                                 |
| fin_calc_year            | date    |                                                                               |
| hub_or_spoke             | integer | Whether the Application is for a Hub or a Spoke location w.r.t. Capital Float |
| in_process_status        | integer |                                                                               |
| is_archived              | integer | Flag indicating whether the Application is archived                           |
| is_fs                    | integer | Flag indicating whether the Application is on FS App                          |
| is_perfios               | integer | Flag indicating whether Perfios auto scraping was opted for by the applicant  |
| last_modified_time       | integer | Last modified timestamp for Application                                       |
| pd_context               | integer | Context of Personal Discussion                                                |
| pd_type                  | integer | Type of Personal Discussion                                                   |
| previous_application_id  | string  | Parent application ID for the application                                     |
| product_type             | integer | Type of Capital Float product associated with the Application. Refer Master.  |
| sl_no                    | integer | Application serial number. Auto generated at Capital Float.                   |
| status                   | integer | Current application status                                                    |
| tags                     | array   | Tags for the application                                                      |
| third_party_reference_id | string  |                                                                               |
| version                  | string  |                                                                               |

**Business Details**

| Name                  | Type    | Description                                                                |
| --------------------- | ------- | -------------------------------------------------------------------------- |
| business_id           | integer | Business entity Id, auto generated at Capital Float                        |
| address_list          | array   | List of business address objects                                           |
| application_context   | integer | Context of association of the business with the application. Refer Master. |
| business_profile      | string  | Information about business                                                 |
| ca_number             | string  | Chartered Accountant number associated with the business                   |
| cibil_request_id      | string  |                                                                            |
| contacts_list         | array   | List of business contact objects                                           |
| incorporation_date    | date    | Incorporation date of the business                                         |
| industry_type         | integer | Industry type of the business. Refer Master                                |
| kyc_status            | integer | Mode of KYC. Refer Master                                                  |
| main_product_category | integer | Main product category of the business. Refer Master                        |
| nature_of_business    | integer | Nature of business. Refer Master                                           |
| operate_as            | integer | Business entity type. Refer Master                                         |
| operation_start_date  | date    | Operation start date of business                                           |
| poi_list              | array   | List of business proof of identity objects                                 |
| registered_name       | string  | Name of Business Entity                                                    |
| services_provided     | array   | List of Services provided. Refer master keys                               |

**Business Financials**

| Name                    | Type    | Description                                           |
| ----------------------- | ------- | ----------------------------------------------------- |
| id                      | integer | Id of the financials, auto generated at Capital Float |
| auto_loan               | float   | Amount of auto loan take by the applicant             |
| base_year               | integer | Base year for financial data                          |
| home_loan               | integer | Amount of home loan take by the applicant             |
| loan_against_property   | integer | Amount of loan against property take by the applicant |
| monthly_emi_obligations | integer | Monthly EMI obligations for the applicant             |
| odcc_limit              | integer | OD/CC limit for the applicant                         |
| outstanding_loan_amount | integer | Outstanding amount of loan for the applicant          |
| personal_loan           | integer | Amount of personal loan take by the applicant         |
| profit_prev_year        | integer | Base -1 year profit for the applicant                 |
| profit_this_year        | integer | Base year profit for the applicant                    |
| turnover_prev_year      | integer | Base -1 year turnover for the applicant               |
| turnover_this_year      | integer | Base year turnover for the applicant                  |
| unsecured_loan          | integer | Amount of unsecured loan taken by the applicant       |

**Ecosystem Details**

| Name               | Type    | Description                                                              |
| ------------------ | ------- | ------------------------------------------------------------------------ |
| ecosystem_id       | integer | Ecosystem ID , auto generated at Capital Float                           |
| branch_code        | string  |                                                                          |
| customer_id        | string  |                                                                          |
| ecosystem_xns_list | array   | List of ecosystem transaction objects                                    |
| is_verified        | integer | Flag indicating whether Ecosystem details for the applicant are verified |
| partner_id         | integer | ID of the Partner against which ecosystem details are to be mapped       |
| partner_name       | string  | Name of the partner against which ecosystem details are to be mapped     |
| password           | string  |                                                                          |
| payment_cycle      | integer | Payment cycle of the applicant with the partner                          |
| rating             | string  | Rating of the applicant with the partner                                 |
| return_percentage  | integer | Return percentage of the applicant on partner’s ecosytem                 |
| start_date         | date    | Relationship start date between Applicant and Partner                    |
| type               | integer | Type of Partner. Refer Master.                                           |
| url                | string  | Applicant’s URL with the partner                                         |
| username           | string  |                                                                          |
| wallet_number      | string  | Wallet number of the applicant with the partner                          |

**Ecosystem Transactions**

| Name                | Type    | Description                                                     |
| ------------------- | ------- | --------------------------------------------------------------- |
| xns_id              | integer | ID of the Transaction auto generated by Capital Float           |
| xn_type             | integer | Transaction type. Refer Master                                  |
| base_month          | integer | Base month against which Ecosystem transaction are to be stored |
| base_month_minus_1  | integer | Ecosystem transaction value for Base Month -1                   |
| base_month_minus_10 | integer | Ecosystem transaction value for Base Month -10                  |
| base_month_minus_11 | integer | Ecosystem transaction value for Base Month -11                  |
| base_month_minus_12 | integer | Ecosystem transaction value for Base Month -12                  |
| base_month_minus_2  | integer | Ecosystem transaction value for Base Month -2                   |
| base_month_minus_3  | integer | Ecosystem transaction value for Base Month -3                   |
| base_month_minus_4  | integer | Ecosystem transaction value for Base Month -4                   |
| base_month_minus_5  | integer | Ecosystem transaction value for Base Month -5                   |
| base_month_minus_6  | integer | Ecosystem transaction value for Base Month -6                   |
| base_month_minus_7  | integer | Ecosystem transaction value for Base Month -7                   |
| base_month_minus_8  | integer | Ecosystem transaction value for Base Month -8                   |
| base_month_minus_9  | integer | Ecosystem transaction value for Base Month -9                   |
| months_of_data      | integer | Number of months of Ecosystem Transactions data                 |

**Fund Use Details**

| Name                 | Type    | Description                                |
| -------------------- | ------- | ------------------------------------------ |
| end_use_id           | integer | End Use ID Auto Generated at Capital Float |
| estimated_cost       | integer |                                            |
| loan_amount_required | integer | Loan amount required by the applicant      |
| usage_type           | integer | Type of Funds Use. Refer Master.           |

**Individual's Details**

| Name                         | Type    | Description                                                                  |
| ---------------------------- | ------- | ---------------------------------------------------------------------------- |
| individual_id                | integer | Individual ID auto generated by Capital Float                                |
| application_context          | integer | Context of association of the individual with the application. Refer Master. |
| birth_date                   | date    | Date of Birth of the Individual                                              |
| business_id                  | integer | Business Entity ID against which this individual is to be mapped             |
| bu_relationship_type         | integer | Relationship of the individual with the Business Entitiy                     |
| bu_share_percent             | integer | Percentage shareholding of the individual with the Business Entity           |
| cibil_consent_flag           | integer | Flag indicating CIBIL consent given by customer                              |
| cibil_consent_mode           | integer | Mode of CIBIL consent. Refer master.                                         |
| cibil_request_id             | integer |                                                                              |
| contacts_list                | array   | List of individual's contacts                                                |
| employer_name                | string  | Name of the Employer for the Individual                                      |
| employment_type              | integer | Type of Employment. Refer Master.                                            |
| father_name                  | string  | Father’s Name for Individual                                                 |
| first_name                   | string  | First Name of the Individual                                                 |
| gender                       | integer | Gender of the Individual                                                     |
| individual_relationship_type | integer |                                                                              |
| kyc_status                   | integer | KYC status for the Individual. Refer Master.                                 |
| last_name                    | string  | Last name of the Individual.                                                 |
| marital_status               | integer | Marital Status of the Individual.                                            |
| mother_name                  | string  | Mother’s Name for Individual.                                                |
| poi_list                     | array   | List of business proof of identity objects                                   |
| qualification                | integer | Qualification of the individual. Refer Master.                               |
| work_ex                      | integer | Work Experience of the individual                                            |

**Bank Details**

| Name            | Type    | Description                                                 |
| --------------- | ------- | ----------------------------------------------------------- |
| acc_id          | integer | Auto generated account ID at Capital Float                  |
| acc_context     | integer | Applicant’s usage of account at Capital Float. Refer Master |
| acc_holder_name | string  | Applicant’s account name                                    |
| acc_no          | string  | Applicant’s account number                                  |
| acc_type        | string  | Applicant’s account type. Refer Master                      |
| bank_name       | string  | Applicant’s repayment bank name                             |
| branch          | string  | Applicant’s repayment bank branch name                      |
| entry_code      | integer |                                                             |
| ifsc_code       | string  | Applicant’s repayment bank IFSC code                        |


## Callbacks
Once an app_id is created. CF will post to your configured Callbacks on registered events.
For now configuration of Callbacks and registration of events is offline. Share these details with CF representative you are in touch with.

` eg: {{your_domain}}/capitalfloat/callback/1`

> Request:

```json

{
    "app_id": "string",
    "offer_type": "string",
    "amount": "string",
    "tenure": "string",
    "interest":"string"
}'
```


**Parameters**

| Name      | Type   | Description                            |
| --------  | ------ | -------------------------------------  |
| app_id    | string | Application Id                         |
| offer_type| string | in_principal_approval, final_approval  |
| amount    | string | Amount                                 |
| tenure    | string | Tenure of the loan                     |
| interest  | string | Interest of the loan                   |

**Events**

| Name                    | Description                       |
| --------------------    | --------------------------------- |
| in_principal_approval   |                                   |
| final_approval          |                                   |
