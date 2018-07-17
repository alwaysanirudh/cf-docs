# Master Key Reference

This section contains the references to all master keys which will be used throughout all API requests.

## Application In Progess Statuses

`metadata.in_process_status`

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

## Application Types

`metadata.application_type`

| Id  | Name                |
| --- | ------------------- |
| 100 | Loan                |
| 200 | Parnter on-boarding |
| 300 | Lender on-boarding  |

## Business Address Types

`business_details[].address_list[].address_type`

| Id   | Name               |
| ---- | ------------------ |
| 2000 | Operating Address  |
| 3000 | Factory Address    |
| 4000 | Registered Address |
| 5000 | Sales Office       |
| 6000 | eKyc               |
| 7000 | Others             |

## Business Industry Types

`business_details[].industry_type`

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

## Perfios Methods

`metadata.is_perfios`

| Id  | Name           |
| --- | -------------- |
| 0   | NA             |
| 100 | Perfios - Bank |
| 200 | Perfios - PDF  |

## PD Contexts

`metadata.pd_context`

| Id  | Name                                       |
| --- | ------------------------------------------ |
| 0   | NA                                         |
| 100 | Low Approval Rate,Low Probability of DPD   |
| 200 | Low Approval Rate,High Probability of DPD  |
| 300 | High Approval Rate,High Probability of DPD |
| 400 | High Approval Rate,Low Probability of DPD  |

## Individual Employment Types

`individual_details[].employment_type`

| Id  | Name          |
| --- | ------------- |
| 0   | Not mentioned |
| 100 | Self employed |
| 200 | Salaried      |
| 300 | Professional  |

## Loan Product Types

`metadata.product_type`

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

## Individual - Business Relationship

Relationship of the individual with the business

`individual_details[].bu_relationship_type`

| Id  | Name       |
| --- | ---------- |
| 0   | NA         |
| 100 | Manager    |
| 200 | Promoter   |
| 300 | Director   |
| 400 | Trustee    |
| 500 | Proprietor |
| 600 | Partner    |

## Individual Marital Statuses

`individual_details[].marital_status`

| Id  | Name     |
| --- | -------- |
| 0   | NA       |
| 100 | Married  |
| 200 | Single   |
| 400 | Divorced |
| 300 | other    |

## Individual POI Types

`individual_details[].poi_list[].id_type`

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

## Bank Account Contexts

`bank_accounts[].acc_context`

| Id  | Name              |
| --- | ----------------- |
| 0   | Not defined       |
| 100 | Disbursal Account |
| 200 | Repayment Account |

## Contact Type

`contact_details[].contact_type`

| Id  | Name     |
| --- | -------- |
| 100 | email    |
| 200 | mobile   |
| 300 | landline |

## Address Active Status

`address_list[].is_active`

| Id  | Name      |
| --- | --------- |
| 0   | NA        |
| 100 | Active    |
| 200 | Inactive  |
| 300 | Ambiguous |
| 400 | Deleted   |

## Individual Application Context

`individual_details.application_context`

| Id  | Name           |
| --- | -------------- |
| 0   | Not defined    |
| 10  | Main applicant |
| 20  | Co-Applicant   |
| 30  | Nominee        |
| 40  | Guarantor      |
| 50  | Reference      |
| 60  | Servicee       |

## User Pool Context

`user_pool_details_models[].pool_context`

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

## Qualification

`individual_details[].qualification`

| Id  | Name          |
| --- | ------------- |
| 0   | None          |
| 100 | 10th Pass     |
| 200 | 12th Pass     |
| 250 | Diploma       |
| 300 | Graduate      |
| 400 | Post Graduate |
| 500 | PHD/Doctorate |

## App Status

`metadata.status`

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

## Main Product Category

`business_details[].main_product_category`

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

## POI type

`business_details[].poi_list[].id_type`

| Id  | Name  |
| --- | ----- |
| 100 | TIN   |
| 200 | GSTIN |
| 300 | PAN   |
| 400 | VAT   |
| 500 | VAT   |

## Application Segment

`metadata.application_segment`

| Id  | Name       |
| --- | ---------- |
| 100 | Business   |
| 200 | Individual |

## Ecosystem Verification Status

`ecosystem_details[].is_verified`

| Id  | Name     |
| --- | -------- |
| 0   | NA       |
| 100 | Verified |

## Cibil Consent Mode

`cibil_consent_mode`

| Id  | Name        |
| --- | ----------- |
| 0   | NA          |
| 100 | email       |
| 200 | missed call |
| 300 | sms         |

## Bank Account Entry Code

`bank_accounts[].entry_code`

| Id  | Name           |
| --- | -------------- |
| 100 | User           |
| 200 | Credit team    |
| 300 | Banking Module |

## Fund Usage Type

`fund_use_details[].usage_type`

| Id   | Name                |
| ---- | ------------------- |
| 100  | Working Capital Gap |
| 200  | Purchase Asset      |
| 300  | Purchase Service    |
| 400  | Expansion Plans     |
| 500  | Bridge Finance      |
| 1000 | Others              |

## Ecosystem Txn type

`ecosystem_details[].ecosystem_xns_list[].xn_type`

| Id  | Name                  |
| --- | --------------------- |
| 0   | NA                    |
| 100 | Sales By Volume       |
| 200 | Sales By Amount       |
| 300 | Purchase by Volume    |
| 400 | Purchase by Amount    |
| 500 | Settlements by Volume |
| 600 | Settlements by Amount |

## PD Type

`metadata.pd_type`

| Id  | Name      |
| --- | --------- |
| 1   | In-person |
| 2   | Physical  |
| 3   | Virtual   |
| 4   | Spoke PD  |
| 5   | NA        |

## Ecosystem type

`ecosystem_details[].type`

| Id   | Name                          |
| ---- | ----------------------------- |
| 100  | Seller on e-commerce site     |
| 200  | Buyer from e-commerce site    |
| 300  | Travel agent                  |
| 400  | Digital payments & remittance |
| 500  | POS                           |
| 600  | Buyer from corporate          |
| 2000 | Others                        |

## Nature of Business

`business_details[].nature_of_business`

| Id  | Name                 |
| --- | -------------------- |
| 0   | NA                   |
| 100 | Distribution/Trading |
| 200 | Services             |
| 300 | Manufacturing        |
| 400 | Retailer             |

## Individual Address Type

`individual_details[].address_list[].address_type`

| Id  | Name              |
| --- | ----------------- |
| 100 | Permanent         |
| 200 | Current           |
| 300 | Address From Ekyc |

## Application Lifecycle Id

`application_lifecycle_id`

| Id  | Name           |
| --- | -------------- |
| 100 | New            |
| 200 | Renewal        |
| 300 | Enhancement    |
| 400 | Re-Application |
| 500 | Cross Sell     |

## App Archived Status

`metadata.is_archived`

| Id  | Name                        |
| --- | --------------------------- |
| 0   | NA                          |
| 100 | Archived for renewal        |
| 200 | Archived due to no interest |

## App Source Name

`metadata.app_source_name`

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

## Entity Type

`business_details.entity_type`

| Id  | Name       |
| --- | ---------- |
| 100 | Business   |
| 200 | Individual |

## Ownership Type

`address_list[].ownership_type`

| Id  | Name             |
| --- | ---------------- |
| 0   | NA               |
| 100 | Owned by self    |
| 200 | Owned by family  |
| 300 | Rented/Leased    |
| 400 | Company Provided |
| 500 | Sharing/PG       |

## Address FI status

`address_list[].is_fi_needed`

| Id  | Name            |
| --- | --------------- |
| 0   | Not Decided     |
| 100 | FI initiated    |
| 200 | FI Re-initiated |
| 300 | FI Completed    |

## Gender

`individual_details[].gender`

| Id  | Name   |
| --- | ------ |
| 0   | NA     |
| 100 | Male   |
| 200 | Female |
| 300 | Others |

## Contact Context

`business_details.contact_context`

| Id  | Name                    |
| --- | ----------------------- |
| 0   | Undefined               |
| 100 | Primary                 |
| 200 | Finance Contact Point   |
| 300 | Collection's contact    |
| 400 | Address owner's contact |
| 500 | Alternate contact       |
| 600 | first choice            |

## Cibil Consent

`individual_details[].cibil_consent_flag`

| Id  | Name           |
| --- | -------------- |
| 0   | NA             |
| 100 | Consent given  |
| 200 | Consent denied |

## Operate As

`business_details[].operate_as`

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

## Hub or Spoke

`metadata.hub_or_spoke`

| Id  | Name  |
| --- | ----- |
| 0   | NA    |
| 100 | Hub   |
| 200 | Spoke |

## Individual - Main applicant Relationship

Relationship of the individual with the main applicant

`individual_details[].individual_relationship_type`

| Id  | Name     |
| --- | -------- |
| 0   | NA       |
| 100 | Father   |
| 200 | Mother   |
| 300 | Husband  |
| 400 | Wife     |
| 500 | Son      |
| 600 | Daughter |

## KYC Status

`business_details[].kyc_status`

| Id  | Name              |
| --- | ----------------- |
| 0   | NA                |
| 99  | Kyc not available |
| 100 | Kyc Available     |
| 200 | Kyc Physical Done |
| 300 | eKyc Done         |

## Is FS

`metadata.is_fs`

| Id          |
| ----------- |
| NA          |
| FS_ELIGIBLE |
| WITH_FS     |
