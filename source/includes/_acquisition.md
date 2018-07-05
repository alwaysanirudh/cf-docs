# Acquisition

## Create Application

Post user creation, the user can now apply for a loan. The loan application is an exhaustive list which accommodates multiple loan types. Not all fields are required.

> Request:

```shell
curl-X POST \
  {{url}}/applications \
  -H "Content-type: application/json"  \
  -H 'Authorization: YOUR_TOKEN' \
  -d '{
    "bank_accounts": [
      {
        "acc_context": 0,
        "acc_holder_name": "string",
        "acc_no": "string",
        "acc_type": "string",
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
            "address_owner": "string",
            "address_type": 0,
            "city": "string",
            "contact_list": [
              {
                "contact_context": 0,
                "contact_information": "string",
                "contact_type": 0
              }
            ],
            "country": 0,
            "district": "string",
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
        "application_context": 0,
        "business_profile": "string",
        "ca_number": "string",
        "cibil_request_id": "string",
        "contacts_list": [
          {
            "contact_context": 0,
            "contact_information": "string",
            "contact_type": 0
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
            "created_time": 0,
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
        "branch_code": "string",
        "customer_id": "string",
        "ecosystem_id": 0,
        "ecosystem_xns_list": [
          {
            "base_month": 0,
            "base_month_minus":[{"month":"1","value":"10000"}]
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
            "city": "string",
            "contact_list": [
              {
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
        "application_context": 0,
        "birth_date": "2018-02-05",
        "bu_relationship_type": 0,
        "bu_share_percent": 0,
        "cibil_consent_flag": 0,
        "cibil_consent_mode": 0,
        "cibil_request_id": "string",
        "contacts_list": [
          {
            "address_id": 0,
            "contact_context": 0,
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
    "metadata": {
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
    "user_pool_details_models": [
      {
        "name": "string",
        "pool_context": 0,
        "user_id": 0,
        "user_pool_id": 0,
        "username": "string"
      }
    ]
  }'
```

> Response:

```json
{
  "app_id": "6d190e91-195f-47b5-bf79-fb86c0792f20"
}
```

`POST {{url}}/applications`

**Application Metadata**

| Name                     | Type    | Description                                                                   |
| ------------------------ | ------- | ----------------------------------------------------------------------------- |
| app_id                   | uuid    | App ID auto generated by Capital Float                                        |
| app_request_id           | string  | The Reference ID at your end for posting the application to Capital Float.    |
| app_source_name          | string  | Source of the application. Refer Master                                       |
| application_lifecycle_id | integer |                                                                               |
| application_segment      | integer | Application Segment (example: Individual/Business). Refer Master.             |
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

| Name             | Type             | Description                                                     |
| ---------------- | ---------------- | --------------------------------------------------------------- |
| xns_id           | integer          | ID of the Transaction auto generated by Capital Float           |
| xn_type          | integer          | Transaction type. Refer Master                                  |
| base_month       | integer          | Base month against which Ecosystem transaction are to be stored |
| base_month_minus | array of objects | Ecosystem transaction value for Base Month -n                   |

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

**in_process_status**

| Id   | Name               |
| ---- | ------------------ |
| 0    | Start              |
| 100  | Page 1             |
| 200  | Consent sms sent   |
| 1000 | Business Page      |
| 2000 | Financials Page    |
| 3000 | Promoter/partner   |
| 4000 | Customer/Supplier  |
| 4001 | Migration specific |
| 5000 | Documents          |

**application_type**

| Id  | Name                |
| --- | ------------------- |
| 100 | Loan                |
| 200 | Parnter on-boarding |
| 300 | Lender on-boarding  |

**business_details[].address_list[].address_type**

| Id   | Name               |
| ---- | ------------------ |
| 2000 | Operating Address  |
| 3000 | Factory Address    |
| 4000 | Registered Address |
| 5000 | Sales Office       |
| 6000 | eKyc               |
| 7000 | Others             |

**business_details[].industry_type**

| Id  | Name                                                                                 |
| --- | ------------------------------------------------------------------------------------ |
| 1   | NA                                                                                   |
| 2   | Auto Service Centres                                                                 |
| 3   | Ayurvedic Clinics/Alternative Medicines                                              |
| 4   | Bars/Gambling Business/Massage Parlours/Beauty Parlours                              |
| 5   | Building material Suppliers/Builder/ Building Contractors                            |
| 6   | Cable Operators/Video Library Owners/Video Parlours                                  |
| 7   | Cold Storage                                                                         |
| 8   | Cyber Cafes                                                                          |
| 9   | DSA, Verification Agencies/Collection Agencies/Repossession Agencies                 |
| 10  | Non IATA Approved Travel Agents                                                      |
| 11  | Finance Companies/Pvt Money Lenders                                                  |
| 12  | Firms/Companies dealing in Chit funds/Nidhi/ Money lending                           |
| 13  | Labour Contractors                                                                   |
| 14  | Manpower Consultants/Placement Agencies                                              |
| 15  | Motor Training Schools                                                               |
| 16  | Mining/Oil Drilling and Refining Business                                            |
| 17  | Real Estate Agents/Brokers                                                           |
| 18  | Security Agencies                                                                    |
| 19  | Stock Brokers                                                                        |
| 20  | Transport Operators with less than 5 Trucks                                          |
| 21  | Vendors that Provide Service to Capital Float                                        |
| 22  | Waste Merchants                                                                      |
| 23  | Commodity traders (agriculture, metal etc...)                                        |
| 24  | Real Estate developers                                                               |
| 25  | Jewellers                                                                            |
| 26  | Steel traders & manufacturing (including forging and rolling mills)                  |
| 27  | Solar panel traders and manufacturing                                                |
| 28  | Educational Institute                                                                |
| 29  | Others                                                                               |
| 31  | Accounting, Book-Keeping And Auditing Activities                                     |
| 32  | Advertising                                                                          |
| 33  | Architectural, Engineering And Other Technical Activities                            |
| 34  | Beauty Parlours & Spa Treatments                                                     |
| 35  | Building Installation and contractor-government                                      |
| 36  | Building Installation and contractor-non government                                  |
| 37  | Business And Management Consultancy Activities                                       |
| 38  | Cargo Handling                                                                       |
| 39  | Ceramic Products                                                                     |
| 40  | Chemical And Fertilizer                                                              |
| 41  | Computers, Computer Peripheral Equipment & Software                                  |
| 42  | Construction Material, Cement, Hardware, Paints And Glass                            |
| 43  | Data Processing                                                                      |
| 44  | Database Activities And Distribution Of Electronic Content                           |
| 45  | Diagnostic and Testing Centres                                                       |
| 46  | DomesticConsumer Appliances                                                          |
| 47  | Dramatic Acts, Music And Other Arts Activities                                       |
| 48  | DSA or commission agents to financial institution                                    |
| 49  | Education-coaching classes                                                           |
| 50  | Education-school & college                                                           |
| 51  | Electronic Parts & Equipments                                                        |
| 52  | Farming Of Cattle, Sheep, Goats, Horses, Asses, Mules And Hinnies; Dairy Farming     |
| 53  | Farming of Food Products                                                             |
| 54  | Financial Activities like Insurance and Pension                                      |
| 55  | Food, Beverage And Tobacco                                                           |
| 56  | Furniture                                                                            |
| 57  | Games And Toys                                                                       |
| 58  | Gas And Refined Petroleum Products                                                   |
| 59  | Glass And Glass Products                                                             |
| 60  | Gold Jewellery And precious metals                                                   |
| 61  | Grain Mill Products                                                                  |
| 62  | Hospital, Nursing Homes and Clinics                                                  |
| 63  | Hotels, Resorts And Camping Sites                                                    |
| 64  | Imitation Jewellery And Related Articles                                             |
| 65  | Investigation And Security Activities                                                |
| 66  | Labour Recruitment And Provision Of Personnel                                        |
| 67  | Leather Goods - Footwear, Luggage, Handbags                                          |
| 68  | Legal Activities                                                                     |
| 69  | Library And Archives Activities                                                      |
| 70  | Liquors, Wines And Malts                                                             |
| 71  | Machinery And Machine Tools                                                          |
| 72  | Market Research And Public Polling                                                   |
| 73  | Metals And Metal Ores-iron & steel                                                   |
| 74  | Metals And Metal Ores-Non iron & steel                                               |
| 75  | Mobile Phones & Accessories                                                          |
| 76  | Motion Picture And Video Production, projection and distribution                     |
| 77  | Motor Vehicles, Motorcycles & other Transport Vehicles                               |
| 78  | OEM & Auto Ancillaries                                                               |
| 79  | Others-Information and Communication                                                 |
| 80  | Paper And Paperboard Products                                                        |
| 81  | Pesticides And Other Agro Chemical Products                                          |
| 82  | Petrol Bunks                                                                         |
| 83  | Pharmaceutical And Medical Goods, Cosmetic And Toilet Articles                       |
| 84  | Pharmaceuticals, Medicinal Chemicals And Botanical Products                          |
| 85  | Photography & Videography Services                                                   |
| 86  | Plastic Products                                                                     |
| 87  | Post & Courier Activities                                                            |
| 88  | Printing of Books and Newspapers                                                     |
| 89  | Publishing Of Books, Brochures, Musical Books And Other Publications                 |
| 90  | Pulp, and printing chemicals                                                         |
| 91  | Quarrying Of Stone, Sand And Clay                                                    |
| 92  | Real Estate Activities On A Fee Or Contract Basis                                    |
| 93  | Renting of Industrial Machinery                                                      |
| 94  | Renting Of Office Machinery And Equipment                                            |
| 95  | Repair And Maintenance                                                               |
| 96  | Restaurants, Bars And Canteens                                                       |
| 97  | Soap & Detergents, Cleaning & Polishing Preparations, Perfumes & Toilet Preparations |
| 98  | Soft Drinks                                                                          |
| 99  | Solid, Liquid And Gaseous Fuels And Related Products                                 |
| 100 | Sporting Activities                                                                  |
| 101 | Storage And Warehousing                                                              |
| 102 | Textile And Wearing Apparel                                                          |
| 103 | Travel Agencies And Tour Operators                                                   |
| 104 | Veneer Sheets, Plywood, Boards                                                       |
| 105 | Veterinary Activities                                                                |
| 106 | Educational Institute                                                                |

**is_perfios**

| Id  | Name           |
| --- | -------------- |
| 0   | NA             |
| 100 | Perfios - Bank |
| 200 | Perfios - PDF  |

**pd_context**

| Id  | Name                                       |
| --- | ------------------------------------------ |
| 0   | NA                                         |
| 100 | Low Approval Rate,Low Probability of DPD   |
| 200 | Low Approval Rate,High Probability of DPD  |
| 300 | High Approval Rate,High Probability of DPD |
| 400 | High Approval Rate,Low Probability of DPD  |

**individual_details[].employment_type**

| Id  | Name          |
| --- | ------------- |
| 0   | Not mentioned |
| 100 | Self employed |
| 200 | Salaried      |
| 300 | Professional  |

**product_type**

| Id   | Name  |
| ---- | ----- |
| 0    | NA    |
| 100  | UBL   |
| 110  | LTUBL |
| 200  | MCA   |
| 300  | PL    |
| 310  | PL+   |
| 320  | iPL   |
| 330  | bPL   |
| 400  | IF    |
| 500  | SCL   |
| 600  | BS    |
| 700  | DR    |
| 800  | TL    |
| 1000 | ECOM  |
| 1100 | FF    |
| 1200 | AB    |
| 1300 | phn   |
| 1400 | Con   |
| 1500 | P     |

**bu_relationship_type**

| Id  | Name       |
| --- | ---------- |
| 0   | NA         |
| 100 | Manager    |
| 200 | Promoter   |
| 300 | Director   |
| 400 | Trustee    |
| 500 | Proprietor |
| 600 | Partner    |

**individual_details[].marital_status**

| Id  | Name     |
| --- | -------- |
| 0   | NA       |
| 100 | Married  |
| 200 | Single   |
| 400 | Divorced |
| 300 | other    |

**individual_details[].poi_list[].id_type**

| Id   | Name            |
| ---- | --------------- |
| 100  | Pan             |
| 200  | Aadhaar         |
| 300  | Driving License |
| 400  | Passport        |
| 500  | Ration Card     |
| 600  | Voter id        |
| 1000 | MRN             |
| 2000 | Taxi Permit     |

**bank_accounts[].acc_context**

| Id  | Name              |
| --- | ----------------- |
| 0   | Not defined       |
| 100 | Disbursal Account |
| 200 | Repayment Account |

**contact_type**

| Id  | Name     |
| --- | -------- |
| 100 | email    |
| 200 | mobile   |
| 300 | landline |

**address_list[].is_active**

| Id  | Name      |
| --- | --------- |
| 0   | NA        |
| 100 | Active    |
| 200 | Inactive  |
| 300 | Ambiguous |
| 400 | Deleted   |

**application_context**

| Id  | Name           |
| --- | -------------- |
| 0   | Not defined    |
| 10  | Main applicant |
| 20  | Co-Applicant   |
| 30  | Nominee        |
| 40  | Guarantor      |
| 50  | Reference      |
| 60  | Servicee       |

**pool_context**

| Id    | Name            |
| ----- | --------------- |
| -1    | root            |
| 0     | not defined     |
| 1000  | creator         |
| 2000  | applicant       |
| 3000  | beneficiary     |
| 4000  | partner         |
| 5000  | agency          |
| 6000  | merchant        |
| 7000  | supplier        |
| 8000  | Sales           |
| 8100  | Sales master    |
| 9000  | Credit          |
| 9100  | Credit master   |
| 10000 | Ops             |
| 10100 | Ops master      |
| 10110 | Ops QC          |
| 10120 | Ops marketplace |
| 10130 | Ops Disburse    |
| 10140 | Ops Banking     |
| 10150 | Ops Compliance  |
| 11000 | BD              |
| 12000 | BST             |

**individual_details[].qualification**

| Id  | Name          |
| --- | ------------- |
| 0   | None          |
| 100 | 10th Pass     |
| 200 | 12th Pass     |
| 250 | Diploma       |
| 300 | Graduate      |
| 400 | Post Graduate |
| 500 | PHD/Doctorate |

**metadata.status**

| Id    | Name                 |
| ----- | -------------------- |
| 0     | not defined          |
| 100   | Lead Created         |
| 110   | Offer Generated      |
| 200   | App in progress      |
| 300   | App Submitted        |
| 400   | App Verified         |
| 450   | COH Decision Pending |
| 500   | Request for login    |
| 600   | File logged-in       |
| 700   | Cam in Progress      |
| 800   | Cam Completed        |
| 900   | Pd in Progress       |
| 1000  | Pd Completed         |
| 1100  | Approved             |
| 1200  | Rejected             |
| 10000 | Disbursed            |
| 11000 | KYC Done             |
| 12000 | CIBIL Pulled         |
| 13000 | Bank Details         |
| 14000 | Loan Agreement Done  |
| 15000 | NACH Done            |
| 16000 | DOC UPLOAD Done      |
| 18000 | Questionnaire Done   |
| 19000 | SHOP_PICTURES_TAKEN  |

**main_product_category**

| Id  | Name                         |
| --- | ---------------------------- |
| 1   | NA                           |
| 2   | Apparels                     |
| 3   | Appliances                   |
| 4   | Automotive                   |
| 5   | Baby Care                    |
| 6   | Bags and Luggage             |
| 7   | Beauty and Personal Care     |
| 8   | Books                        |
| 9   | Cameras and Accessories      |
| 10  | Eyewear                      |
| 11  | Fashion Accessories          |
| 12  | Footwear                     |
| 13  | Fragrances                   |
| 14  | Furniture                    |
| 15  | Gaming                       |
| 16  | Gifting Events               |
| 17  | Hardware & Sanitary Fittings |
| 18  | Health, Wellness & Medicine  |
| 19  | Hobbies                      |
| 20  | Home Decor                   |
| 21  | Home Furnishing              |
| 22  | Home Improvement             |
| 23  | Jewellery                    |
| 24  | Kids Wear                    |
| 25  | Kitchenware                  |
| 26  | Mobiles and Tablets          |
| 27  | Movies and Music             |
| 28  | Musical Instruments          |
| 29  | Mens Ethnic Wear             |
| 30  | Nutrition & Supplements      |
| 31  | Office Equipment             |
| 32  | Online Education             |
| 33  | Sports & Fitness             |
| 34  | Stationery                   |
| 35  | Toys & Games                 |
| 36  | TVs, Audio and Video         |
| 37  | Watches                      |
| 38  | Women Ethnic Wear            |
| 39  | Other                        |

**business_details[].poi_list[].id_type**

| Id  | Name  |
| --- | ----- |
| 100 | TIN   |
| 200 | GSTIN |
| 300 | PAN   |
| 400 | VAT   |
| 500 | VAT   |

**application_segment**

| Id  | Name       |
| --- | ---------- |
| 100 | Business   |
| 200 | Individual |

**ecosystem_details[].is_verified**

| Id  | Name     |
| --- | -------- |
| 0   | NA       |
| 100 | Verified |

**cibil_consent_mode**

| Id  | Name        |
| --- | ----------- |
| 0   | NA          |
| 100 | email       |
| 200 | missed call |
| 300 | sms         |

**bank_accounts[].entry_code**

| Id  | Name           |
| --- | -------------- |
| 100 | User           |
| 200 | Credit team    |
| 300 | Banking Module |

**fund_use_details[].usage_type**

| Id   | Name                |
| ---- | ------------------- |
| 100  | Working Capital Gap |
| 200  | Purchase Asset      |
| 300  | Purchase Service    |
| 400  | Expansion Plans     |
| 500  | Bridge Finance      |
| 1000 | Others              |

**ecosystem_details[].ecosystem_xns_list[].xn_type**

| Id  | Name                  |
| --- | --------------------- |
| 0   | NA                    |
| 100 | Sales By Volume       |
| 200 | Sales By Amount       |
| 300 | Purchase by Volume    |
| 400 | Purchase by Amount    |
| 500 | Settlements by Volume |
| 600 | Settlements by Amount |

**pd_type**

| Id  | Name      |
| --- | --------- |
| 1   | In-person |
| 2   | Physical  |
| 3   | Virtual   |
| 4   | Spoke PD  |
| 5   | NA        |

**ecosystem_details[].type**

| Id   | Name                          |
| ---- | ----------------------------- |
| 100  | Seller on e-commerce site     |
| 200  | Buyer from e-commerce site    |
| 300  | Travel agent                  |
| 400  | Digital payments & remittance |
| 500  | POS                           |
| 600  | Buyer from corporate          |
| 2000 | Others                        |

**nature_of_business**

| Id  | Name                 |
| --- | -------------------- |
| 0   | NA                   |
| 100 | Distribution/Trading |
| 200 | Services             |
| 300 | Manufacturing        |
| 400 | Retailer             |

**individual_details[].address_list[].address_type**

| Id  | Name              |
| --- | ----------------- |
| 100 | Permanent         |
| 200 | Current           |
| 300 | Address From Ekyc |

**application_lifecycle_id**

| Id  | Name           |
| --- | -------------- |
| 100 | New            |
| 200 | Renewal        |
| 300 | Enhancement    |
| 400 | Re-Application |
| 500 | Cross Sell     |

**is_archived**

| Id  | Name                        |
| --- | --------------------------- |
| 0   | NA                          |
| 100 | Archived for renewal        |
| 200 | Archived due to no interest |

**app_source_name**

| Id  | Name                   |
| --- | ---------------------- |
| 1   | web_app_form           |
| 2   | abcde                  |
| 3   | fs_app_form            |
| 4   | cl_app_form            |
| 5   | dsa_loan_app_form      |
| 6   | mlp_web_form           |
| 7   | dsa_ondoarding_form    |
| 8   | api_integration_amazon |
| 9   | api_integration        |
| 10  | third_party_referral   |
| 11  | moonshot               |
| 12  | one_click_enhancement  |
| 13  | taxi_app_form          |
| 14  | checkout_finance       |
| 15  | api_integration_pl     |

**entity_type**

| Id  | Name       |
| --- | ---------- |
| 100 | Business   |
| 200 | Individual |

**ownership_type**

| Id  | Name             |
| --- | ---------------- |
| 0   | NA               |
| 100 | Owned by self    |
| 200 | Owned by family  |
| 300 | Rented/Leased    |
| 400 | Company Provided |
| 500 | Sharing/PG       |

**is_fi_needed**

| Id  | Name            |
| --- | --------------- |
| 0   | Not Decided     |
| 100 | FI initiated    |
| 200 | FI Re-initiated |
| 300 | FI Completed    |

**individual_details[].gender**

| Id  | Name   |
| --- | ------ |
| 0   | NA     |
| 100 | Male   |
| 200 | Female |
| 300 | Others |

**contact_context**

| Id  | Name                    |
| --- | ----------------------- |
| 0   | Undefined               |
| 100 | Primary                 |
| 200 | Finance Contact Point   |
| 300 | Collection's contact    |
| 400 | Address owner's contact |
| 500 | Alternate contact       |
| 600 | first choice            |

**cibil_consent_flag**

| Id  | Name           |
| --- | -------------- |
| 0   | NA             |
| 100 | Consent given  |
| 200 | Consent denied |

**business_details[].operate_as**

| Id   | Name                       |
| ---- | -------------------------- |
| 0    | Other                      |
| 100  | Sole Proprietorship        |
| 200  | Partnership                |
| 300  | LLP                        |
| 400  | Private Limited            |
| 500  | LLC                        |
| 600  | One Director Company       |
| 700  | Co-operative Society       |
| 800  | Government                 |
| 900  | Hindu Undivided family     |
| 1000 | Not Classified             |
| 1100 | Public Limited             |
| 1150 | Limited Company (Unlisted) |
| 1200 | Self help group            |
| 1300 | Trust                      |

**hub_or_spoke**

| Id  | Name  |
| --- | ----- |
| 0   | NA    |
| 100 | Hub   |
| 200 | Spoke |

**individual_relationship_type**

| Id  | Name     |
| --- | -------- |
| 0   | NA       |
| 100 | Father   |
| 200 | Mother   |
| 300 | Husband  |
| 400 | Wife     |
| 500 | Son      |
| 600 | Daughter |

**business_details[].kyc_status**

| Id  | Name              |
| --- | ----------------- |
| 0   | NA                |
| 99  | Kyc not available |
| 100 | Kyc Available     |
| 200 | Kyc Physical Done |
| 300 | eKyc Done         |

**is_fs**

| Id          |
| ----------- |
| NA          |
| FS_ELIGIBLE |
| WITH_FS     |

## Create User

A user needs to be created on Capital Float's system for a loan application

> Request:

```shell
curl -X POST \
  {{url}}/users \
  -H "Content-type: application/json"  \
  -H 'Authorization: YOUR_TOKEN' \
  -d '{
    "username": "string",
    "phone": "string",
    "city": "string",
    "app_id": "string",
    "send_welcome_email": 1,
    "name": "string"
  }'
```

> Response:

```json
If the request was successful

{
  "status": 200,
  "message": "user successfully created"
}

If the request was denied

{
  "status": 400,
  "message": "username, phone, app_id are mandatory parameters"
}
```

`POST {{url}}/users`

**Parameters**

| Name               | Type    | Mandatory | Description                      |
| ------------------ | ------- | --------- | -------------------------------- |
| name               | string  | Yes       | User's name                      |
| username           | string  | Yes       | User's username/email            |
| phone              | string  | Yes       | User's phone                     |
| app_id             | string  | Yes       | app_id from application created  |
| city               | string  | No        | User's current city              |
| send_welcome_email | integer | No        | Send welcome Email to user (0/1) |
