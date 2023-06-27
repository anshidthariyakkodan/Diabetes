# Diabetes
> The Health Facts database (Cerner Corporation, Kansas City, MO), a national data warehouse that collects comprehensive clinical records across hospitals throughout the United States. The actual database contain all patient’s data but specifically I wanted to work with Diabetes related data.
---
## Feature details

| Row no | Feature name                 | Type    | Description and values                                                                       |
|--------|------------------------------|---------|----------------------------------------------------------------------------------------------|
| 0      | Encounter ID                 | Numeric | Unique identifier of an encounter                                                            |
| 1      | Patient number               | Numeric | Unique identifier of a patient                                                               |
| 2      | Race                         | Nominal | Values: Caucasian, Asian, African American, Hispanic, and other                             |
| 3      | Gender                       | Nominal | Values: male, female, and unknown/invalid                                                   |
| 4      | Age                          | Nominal | Grouped in 10-year intervals: [0, 10), [10, 20), ..., [90, 100)                              |
| 5      | Weight                       | Numeric | Weight in pounds                                                                             |
| 6*     | Admission type               | Nominal | Integer identifier corresponding to 9 distinct values                                        |
| 7*     | Discharge disposition        | Nominal | Integer identifier corresponding to 29 distinct values                                       |
| 8*     | Admission source             | Nominal | Integer identifier corresponding to 21 distinct values                                       |
| 9      | Time in hospital             | Numeric | Integer number of days between admission and discharge                                       |
| 10*    | Payer code                   | Nominal | Integer identifier corresponding to 23 distinct values                                       |
| 11*    | Medical specialty            | Nominal | Integer identifier of a specialty of the admitting physician                                |
| 12     | Number of lab procedures     | Numeric | Number of lab tests performed during the encounter                                           |
| 13     | Number of procedures         | Numeric | Number of procedures (other than lab tests) performed during the encounter                   |
| 14     | Number of medications        | Numeric | Number of distinct generic names administered during the encounter                           |
| 15     | Number of outpatient visits  | Numeric | Number of outpatient visits of the patient in the year preceding the encounter               |
| 16     | Number of emergency visits   | Numeric | Number of emergency visits of the patient in the year preceding the encounter                |
| 17     | Number of inpatient visits   | Numeric | Number of inpatient visits of the patient in the year preceding the encounter                |
| 18     | Diagnosis 1                  | Nominal | The primary diagnosis (coded as first three digits of ICD9)                                  |
| 19     | Diagnosis 2                  | Nominal | Secondary diagnosis (coded as first three digits of ICD9)                                    |
| 20     | Diagnosis 3                  | Nominal | Additional secondary diagnosis (coded as first three digits of ICD9)                         |
| 21     | Number of diagnoses          | Numeric | Number of diagnoses entered into the system                                                  |
| 22     | Glucose serum test result    | Nominal | Indicates the range of the result or if the test was not taken                               |
| 23     | A1c test result              | Nominal | Indicates the range of the result or if the test was not taken                               |
| 24     | Change of medications        | Nominal | Indicates if there was a change in diabetic medications (either dosage or generic name)      |
| 25     | Diabetes medications         | Nominal | Indicates if there was any diabetic medication prescribed                                    |
| 26*    | 24 features for medications | Nominal | For the generic names and dosage changes, indicates whether the drug was prescribed or changed|
| 27     | Readmitted                   | Nominal | Days to inpatient readmission                                                                |

**24 features for medications**:
_Metformin, Repaglinide, Nateglinide, Chlorpropamide, Glimepiride, Acetohexamide, Glipizide, Glyburide, Tolbutamide, Pioglitazone, Rosiglitazone, Acarbose, Miglitol, Troglitazone, Tolazamide, Insulin, Glyburide-metformin, Glipizide-metformin, Glimepiride-pioglitazone, Metformin-rosiglitazone, Metformin-pioglitazone_  
Values: “up” if the dosage was increased during the encounter, “down” if the dosage was decreased, “steady” if the dosage did not change, and “no” if the drug was not prescribed

### Categories in admission type column(admission_type_id)
1: Emergency  
2: Urgent  
3: Elective  
4: New born  
5: Not Available  
6: NULL  
7: Trauma Center  
8: Not Mapped  

### Categories in discharge type column(discharge_disposition_id)
1 Discharged to home\
2 Discharged/transferred to another short term hospital\
3 Discharged/transferred to SNF\
4 Discharged/transferred to ICF\
5 Discharged/transferred to another type of inpatient care institution\
6 Discharged/transferred to home with home health service\
7 Left AMA\
8 Discharged/transferred to home under care of Home IV provider\
9 Admitted as an inpatient to this hospital\
10 Neonate discharged to another hospital for neonatal aftercare\
11 Expired\
12 Still patient or expected to return for outpatient services\
13 Hospice / home\
14 Hospice / medical facility\
15 Discharged/transferred within this institution to Medicare approved swing bed\
16 Discharged/transferred/referred another institution for outpatient services\
17 Discharged/transferred/referred to this institution for outpatient services\
18 NULL\
19 Expired at home. Medicaid only, hospice.\
20 Expired in a medical facility. Medicaid only, hospice.\
21 Expired, place unknown. Medicaid only, hospice.\
22 Discharged/transferred to another rehab fac including rehab units of a hospital .\
23 Discharged/transferred to a long term care hospital.\
24 Discharged/transferred to a nursing facility certified under Medicaid but not certified under Medicare.\
25 Not Mapped\
26 Unknown/Invalid\
30 Discharged/transferred to another Type of Health Care Institution not Defined Elsewhere\
27 Discharged/transferred to a federal health care facility.\
28 Discharged/transferred/referred to a psychiatric hospital of psychiatric distinct part unit of a hospital\
29 Discharged/transferred to a Critical Access Hospital (CAH).\

### Admission source column(admission_source_id)
1 Physician Referral\
2 Clinic Referral\
3 HMO Referral\
4 Transfer from a hospital\
5 Transfer from a Skilled Nursing Facility (SNF)\
6 Transfer from another health care facility\
7 Emergency Room\
8 Court/Law Enforcement\
9 Not Available\
10 Transfer from critial access hospital\
11 Normal Delivery\
12 Premature Delivery\
13 Sick Baby\
14 Extramural Birth\
15 Not Available\
17 NULL\
18 Transfer From Another Home Health Agency\
19 Readmission to Same Home Health Agency\
20 Not Mapped\
21 Unknown/Invalid\
22 Transfer from hospital inpt/same fac reslt in a sep claim\
23 Born inside this hospital\
24 Born outside this hospital\
25 Transfer from Ambulatory Surgery Center\
26 Transfer from Hospice\
In payer code and Medical Speciality the missing values are very high so they are not considered generally so the description for each code is not provided
