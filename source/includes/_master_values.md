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

## Individual Business Relationship Types

| id  | label      | name       |
| --- | ---------- | ---------- |
| 0   | NA         | NA         |
| 100 | Manager    | MANAGER    |
| 200 | Promoter   | PROMOTER   |
| 300 | Director   | DIRECTOR   |
| 400 | Trustee    | TRUSTEE    |
| 500 | Proprietor | PROPRIETOR |
| 600 | Partner    | PARTNER    |

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
