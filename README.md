# Analysis of Houston Parking Citations




### Enviroment
- Windows Linux Subsystem
- anaconda distribution

## Running repo

1. clone repo & cd to project folder

```shell
git clone https://github.com/franksalas/parking_citation_analysis.git


cd parking_citation_analysis
```

2. create enviroment from yml file

```shell
conda env create -f environment.yml
```

3. activate enviroment

```shell
source activate parking
```
4. get to work

## Metadata

| Column                    | Description                                                                                                                                                                                                                                                                                                                           |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CON_UID                   | System generated unique identifier for the parking citation                                                                                                                                                                                                                                                                           |
| Entity_UID                | Unique ID for the entity that received the parking citation. Sometimes an individual or company can have multiple entity IDs due to matching issues.                                                                                                                                                                                  |
| Vehicle_Plate_Anon        | An anonymized version of the plate number. This anonymized number will always be consistent across files released on the same date (i.e. all files released on 5/1/2016) but may change from one release to the next (i.e. the assigned number may change 5/1/2016 to the 5/1/2017 release) to  ensure anonymity                      |
| Invoice_Number            | The unique citation's number commonly referred to by the customer and Parking Management                                                                                                                                                                                                                                              |
| Invoice_Date              | The date the citation was issued (usually the event date, but sometimes re-issued afterwards if a new owner is found)                                                                                                                                                                                                                 |
| Invoice_Due_Date          | The due date of the citation's payment                                                                                                                                                                                                                                                                                                |
| Entity_Type               | The type of entity receiving the citation                                                                                                                                                                                                                                                                                             |
| Billing_State_Abbrev      | The state the entity resides in                                                                                                                                                                                                                                                                                                       |
| Billing_Postal_Code       | The zip code the entity receiving the parking citation resides in                                                                                                                                                                                                                                                                     |
| Event_Block_Number        | The city block the citation was issued in                                                                                                                                                                                                                                                                                             |
| Event_Street              | The city street the citation was issued on                                                                                                                                                                                                                                                                                            |
| Event_Date                | The issue date of the citation                                                                                                                                                                                                                                                                                                        |
| Citation_Status           | The current status of the citation                                                                                                                                                                                                                                                                                                    |
| Meter_Violation           | Whether the citation is tied directly to a meter violation (0=False or unknown/ 1=true)                                                                                                                                                                                                                                               |
| Meter_Number              | The meter number associated with the violation                                                                                                                                                                                                                                                                                        |
| Citation_Description_Code | The code for why the citation was issued                                                                                                                                                                                                                                                                                              |
| Citation_Description      | Description of why the citation was issued                                                                                                                                                                                                                                                                                            |
| VIC_LEGAL_DESCRIPTION     | Legal description of why the citation was issued                                                                                                                                                                                                                                                                                      |
| CON_IS_WRITEOFF           | Was the citation written off (0=false/1=true)                                                                                                                                                                                                                                                                                         |
| CON_IS_WARNING            | Is the citation a warning rather than a fine (0=false/1=true)                                                                                                                                                                                                                                                                         |
| CON_IS_VOID               | Has the citation been voided (0=false/1=true)                                                                                                                                                                                                                                                                                         |
| CON_IS_UNDER_APPEAL       | Is the citation under appeal (0=false/1=true)                                                                                                                                                                                                                                                                                         |
| CON_IS_UNCOLLECTABLE      | Is the citation uncollectable (0=false/1=true)                                                                                                                                                                                                                                                                                        |
| CON_IS_SPECIAL_STATUS     | Does the citation has a special status (0=false/1=true)                                                                                                                                                                                                                                                                               |
| CON_IS_SOURCE_MANUAL      | Was the citation manually entered into the parking management system (0=false/1=true). This usually occurs for older tickets that were issued prior to the implementation of T2 when a customer comes in voluntarily to pay. This can also happen when a volunteer issues a handicap parking citation or a handheld device is broken. |
| CON_IS_PREENTERED         |                                                                                                                                                                                                                                                                                                                                       |
| CON_IS_ON_ADMIN_HOLD      | Is the citation on administrative hold (0=false/1=true)                                                                                                                                                                                                                                                                               |
| CON_IS_NO_CONTEST         |                                                                                                                                                                                                                                                                                                                                       |
| Initial_Citation_Amount   | The initial amount (or face value) of the citation when it was issued                                                                                                                                                                                                                                                                 |
| Amount_Outstanding        | The amount currently due, including any delinquent collection fees imposed                                                                                                                                                                                                                                                            |
| Citation_Officer          | Issuing Officer                                                                                                                                                                                                                                                                                                                       |
| Citation_Officer_UID      | Issue Officer's unique identifier in the system                                                                                                                                                                                                                                                                                       |
| Vehicle_Make              |                                                                                                                                                                                                                                                                                                                                       |
| Vehicle_Year              |                                                                                                                                                                                                                                                                                                                                       |
| Vehicle_Style             |                                                                                                                                                                                                                                                                                                                                       |
| Latitude                  | The latitude reported by the handheld device. Handheld devices started reporting issuing location in mid-2014 but sometimes the coordinators are not captured                                                                                                                                                                         |
| Longitude                 | The longitude reported by the handheld device. Handheld devices started reporting issuing location in mid-2014 but sometimes the coordinators are not captured                                                                                                                                                                        |