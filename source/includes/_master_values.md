# Master Key Reference

This section contains the references to all master keys which will be used throughout all API requests.

## Application In Progess Statuses

| id   | label             | name              |
| ---- | ----------------- | ----------------- |
| 0    | Start             | START             |
| 100  | Page 1            | PAGE_ONE          |
| 200  | Consent sms sent  | CONSENT_SMS_SENT  |
| 1000 | Business Page     | BUSINESS_PAGE     |
| 2000 | Financials Page   | FINANCIALS        |
| 3000 | Promoter/partner  | PROMOTER_PARTNER  |
| 4000 | Customer/Supplier | CUSTOMER_SUPPLIER |
| 5000 | Documents         | DOCUMENTS         |

## Application Types

| id  | label               | name                |
| --- | ------------------- | ------------------- |
| 100 | Loan                | LOAN                |
| 200 | Parnter on-boarding | PARTNER_ON_BOARDING |
| 300 | Lender on-boarding  | LENDER_ON_BOARDING  |

## Business Address Types

| id   | label              | name         |
| ---- | ------------------ | ------------ |
| 2000 | Operating Address  | OPERATING    |
| 3000 | Factory Address    | FACTORY      |
| 4000 | Registered Address | REGISTERED   |
| 5000 | Sales Office       | SALES_OFFICE |
| 6000 | eKyc               | EKYC         |
| 7000 | Others             | OTHERS       |

## Business Industry Types

| id  | label                                                                | name                                                                 |
| --- | -------------------------------------------------------------------- | -------------------------------------------------------------------- |
| 1   | NA                                                                   | NA                                                                   |
| 2   | Auto Service Centres                                                 | Auto Service Centres                                                 |
| 3   | Ayurvedic Clinics/Alternative Medicines                              | Ayurvedic Clinics/Alternative Medicines                              |
| 4   | Bars/Gambling Business/Massage Parlours/Beauty Parlours              | Bars/Gambling Business/Massage Parlours/Beauty Parlours              |
| 5   | Building material Suppliers/Builder/ Building Contractors            | Building material Suppliers/Builder/ Building Contractors            |
| 6   | Cable Operators/Video Library Owners/Video Parlours                  | Cable Operators/Video Library Owners/Video Parlours                  |
| 7   | Cold Storage                                                         | Cold Storage                                                         |
| 8   | Cyber Cafes                                                          | Cyber Cafes                                                          |
| 9   | DSA, Verification Agencies/Collection Agencies/Repossession Agencies | DSA, Verification Agencies/Collection Agencies/Repossession Agencies |
| 10  | Non IATA Approved Travel Agents                                      | Non IATA Approved Travel Agents                                      |
| 11  | Finance Companies/Pvt Money Lenders                                  | Finance Companies/Pvt Money Lenders                                  |
| 12  | Firms/Companies dealing in Chit funds/Nidhi/ Money lending           | Firms/Companies dealing in Chit funds/Nidhi/ Money lending           |
| 13  | Labour Contractors                                                   | Labour Contractors                                                   |
| 14  | Manpower Consultants/Placement Agencies                              | Manpower Consultants/Placement Agencies                              |
| 15  | Motor Training Schools                                               | Motor Training Schools                                               |
| 16  | Mining/Oil Drilling and Refining Business                            | Mining/Oil Drilling and Refining Business                            |
| 17  | Real Estate Agents/Brokers                                           | Real Estate Agents/Brokers                                           |
| 18  | Security Agencies                                                    | Security Agencies                                                    |
| 19  | Stock Brokers                                                        | Stock Brokers                                                        |
| 20  | Transport Operators with less than 5 Trucks                          | Transport Operators with less than 5 Trucks                          |
| 21  | Vendors that Provide Service to Capital Float                        | Vendors that Provide Service to Capital Float                        |
| 22  | Waste Merchants                                                      | Waste Merchants                                                      |
| 23  | Commodity traders (agriculture, metal etc...)                        | Commodity traders (agriculture, metal etc...)                        |
| 24  | Real Estate developers                                               | Real Estate developers                                               |
| 25  | Jewellers                                                            | Jewellers                                                            |
| 26  | Steel traders & manufacturing (including forging and rolling mills)  | Steel traders & manufacturing (including forging and rolling mills)  |
| 27  | Solar panel traders and manufacturing                                | Solar panel traders and manufacturing                                |
| 28  | Educational Institute                                                | Educational Institute                                                |
| 29  | Others                                                               | Others                                                               |

## Perfios Methods

| id  | label          | name                        |
| --- | -------------- | --------------------------- |
| 0   | NA             | NA                          |
| 100 | Perfios - Bank | PERFIOS_BY_BANK_CREDENTIALS |
| 200 | Perfios - PDF  | PERFIOS_BY_PDF              |

## PD Contexts

| pd_context |
| ---------- |
| NA         |
| LOW_LOW    |
| LOW_HIGH   |
| HIGH_HIGH  |
| HIGH_LOW   |

## Individual Employment Types

| id  | label         | name          |
| --- | ------------- | ------------- |
| 0   | Not mentioned | NONE          |
| 100 | Self employed | SELF_EMPLOYED |
| 200 | Salaried      | SALARIED      |
| 300 | Professional  | PROFESSIONAL  |

## Loan Product Types

| id   | label | name |
| ---- | ----- | ---- |
| 0    | NA    | NA   |
| 100  | UBL   | UBL  |
| 200  | MCA   | MCA  |
| 300  | PL    | PL   |
| 310  | PL+   | PLP  |
| 320  | iPL   | IPL  |
| 330  | bPL   | BPL  |
| 400  | IF    | IF   |
| 500  | SCL   | SCL  |
| 600  | BS    | BS   |
| 700  | DR    | DR   |
| 800  | TL    | TL   |
| 900  | Veh   | VH   |
| 1000 | ECOM  | ECOM |
| 1100 | FF    | FF   |
| 1200 | AB    | AB   |

## Individual Marital Statuses

| id  | label    | name      |
| --- | -------- | --------- |
| 0   | NA       | NA        |
| 100 | Married  | MARRIED   |
| 200 | Single   | UNMARRIED |
| 400 | Divorced | DIVORCED  |
| 300 | other    | OTHER     |

## Individual POI Types

| id   | label           | name            |
| ---- | --------------- | --------------- |
| 100  | Pan             | PAN             |
| 200  | Aadhaar         | AADHAAR         |
| 300  | Driving License | DRIVING_LICENSE |
| 400  | Passport        | PASSPORT        |
| 500  | Ration Card     | RATION_CARD     |
| 600  | Voter id        | VOTER_ID        |
| 1000 | MRN             | DR_REG_NO       |
| 2000 | Taxi Permit     | TAXI_PERMIT     |

## Bank Account Contexts

| id  | label             | name              |
| --- | ----------------- | ----------------- |
| 0   | Not defined       | NONE              |
| 100 | Disbursal Account | DISBURSAL_ACCOUNT |
| 200 | Repayment Account | REPAYMENT_ACCOUNT |

## Operate As

`business_details.operate_as`

| id   | label                      | name                    |
| ---- | -------------------------- | ----------------------- |
| 0    | Other                      | OTHER                   |
| 100  | Sole Proprietorship        | SOLE_PROPRIETORSHIP     |
| 200  | Partnership                | PARTNERSHIP             |
| 300  | LLP                        | LLP                     |
| 400  | Private Limited            | PRIVATE_LIMITED         |
| 500  | LLC                        | LLC                     |
| 600  | One Director Company       | ONE_DIRECTOR_COMPANY    |
| 700  | Co-operative Society       | CO_OPERATIVE_SOCIETY    |
| 800  | Government                 | GOVERNMENT              |
| 900  | Hindu Undivided family     | HINDU_UNDIVIDED_FAMILY  |
| 1000 | Not Classified             | NOT_CLASSIFIED          |
| 1100 | Public Limited             | PUBLIC_LIMITED          |
| 1150 | Limited Company (Unlisted) | PUBLIC_LIMITED_UNLISTED |
| 1200 | Self help group            | SELF_HELP_GROUP         |
| 1300 | Trust                      | TRUST                   |

## Nature of Business

`business_details.nature_of_business`

| id  | label                | name                 |
| --- | -------------------- | -------------------- |
| 0   | NA                   | NA                   |
| 100 | Distribution/Trading | DISTRIBUTION_TRADING |
| 200 | Services             | SERVICES             |
| 300 | Manufacturing        | MANUFACTURING        |
| 400 | Retailer             | RETAILER             |

## Main Product Category

`business_details.main_product_category`

| id  | label                        | name                         |
| --- | ---------------------------- | ---------------------------- |
| 1   | NA                           | NA                           |
| 2   | Apparels                     | Apparels                     |
| 3   | Appliances                   | Appliances                   |
| 4   | Automotive                   | Automotive                   |
| 5   | Baby Care                    | Baby Care                    |
| 6   | Bags and Luggage             | Bags and Luggage             |
| 7   | Beauty and Personal Care     | Beauty and Personal Care     |
| 8   | Books                        | Books                        |
| 9   | Cameras and Accessories      | Cameras and Accessories      |
| 10  | Eyewear                      | Eyewear                      |
| 11  | Fashion Accessories          | Fashion Accessories          |
| 12  | Footwear                     | Footwear                     |
| 13  | Fragrances                   | Fragrances                   |
| 14  | Furniture                    | Furniture                    |
| 15  | Gaming                       | Gaming                       |
| 16  | Gifting Events               | Gifting Events               |
| 17  | Hardware & Sanitary Fittings | Hardware & Sanitary Fittings |
| 18  | Health, Wellness & Medicine  | Health, Wellness & Medicine  |
| 19  | Hobbies                      | Hobbies                      |
| 20  | Home Decor                   | Home Decor                   |
| 21  | Home Furnishing              | Home Furnishing              |
| 22  | Home Improvement             | Home Improvement             |
| 23  | Jewellery                    | Jewellery                    |
| 24  | Kids Wear                    | Kids Wear                    |
| 25  | Kitchenware                  | Kitchenware                  |
| 26  | Mobiles and Tablets          | Mobiles and Tablets          |
| 27  | Movies and Music             | Movies and Music             |
| 28  | Musical Instruments          | Musical Instruments          |
| 29  | Mens Ethnic Wear             | Mens Ethnic Wear             |
| 30  | Nutrition & Supplements      | Nutrition & Supplements      |
| 31  | Office Equipment             | Office Equipment             |
| 32  | Online Education             | Online Education             |
| 33  | Sports & Fitness             | Sports & Fitness             |
| 34  | Stationery                   | Stationery                   |
| 35  | Toys & Games                 | Toys & Games                 |
| 36  | TVs, Audio and Video         | TVs, Audio and Video         |
| 37  | Watches                      | Watches                      |
| 38  | Women Ethnic Wear            | Women Ethnic Wear            |
| 39  | Other                        | Other                        |

## Contact Context

`business_details.contact_context`

| id  | label                   | name                |
| --- | ----------------------- | ------------------- |
| 0   | Undefined               | UNDEFINED           |
| 100 | Primary                 | PRIMARY             |
| 200 | Finance Contact Point   | FINANCE_CONTACT     |
| 300 | Collection's contact    | COLLECTIONS_CONTACT |
| 400 | Address owner's contact | ADDRESS_CONTACT     |
| 500 | Alternate contact       | ALTERNATE           |
| 600 | first choice            | FIRST_CHOICE        |

## Entity Type

`business_details.entity_type`

| id  | label      | name       |
| --- | ---------- | ---------- |
| 100 | Business   | BUSINESS   |
| 200 | Individual | INDIVIDUAL |

## Qualification

`individual_details.qualification`

| id  | label         | name          |
| --- | ------------- | ------------- |
| 0   | None          | NA            |
| 100 | 10th Pass     | \_10TH        |
| 200 | 12th Pass     | \_12TH        |
| 250 | Diploma       | DIPLOMA       |
| 300 | Graduate      | GRADUATE      |
| 400 | Post Graduate | POST_GRADUATE |
| 500 | PHD/Doctorate | PHD           |

## Individual - Business Relationship

Relationship of the individual with the business

`individual_details.bu_relationship_type`

| id  | label      | name       |
| --- | ---------- | ---------- |
| 0   | NA         | NA         |
| 100 | Manager    | MANAGER    |
| 200 | Promoter   | PROMOTER   |
| 300 | Director   | DIRECTOR   |
| 400 | Trustee    | TRUSTEE    |
| 500 | Proprietor | PROPRIETOR |
| 600 | Partner    | PARTNER    |

## Individual - Main applicant Relationship

Relationship of the individual with the main applicant

`individual_details.individual_relationship_type`

| id  | label    | name     |
| --- | -------- | -------- |
| 0   | NA       | NA       |
| 100 | Father   | FATHER   |
| 200 | Mother   | MOTHER   |
| 300 | Husband  | HUSBAND  |
| 400 | Wife     | WIFE     |
| 500 | Son      | SON      |
| 600 | Daughter | DAUGHTER |
