# Diabetes
The Health Facts database (Cerner Corporation, Kansas City, MO), a national data warehouse that collects comprehensive clinical records across hospitals throughout the United States. The actual database contain all patient’s data but specifically I wanted to work with Diabetes related data.

It is an inpatient encounter (a hospital admission)
It is a “diabetic” encounter, that is, one during which any kind of diabetes was entered the system as a diagnosis.
The length of stay was at least 1 day and at most 14 days.
Laboratory tests were performed during the encounter.
Medications were administered during the encounter. Almost 1 Lakh records were found to be satisfying the above five criterias and the dataset has 55 features like gender, weight, encounter_id, readmitted. Dataset can be used for Classification and Clustering tasks. I will be using it for predicting whether the patient will readmit within 30 days or not. That is a classification task.
Here We have provided short description of each feature.

Encounter ID Unique identifier of an encounter
Patient number Unique identifier of a patient
Race Values: Caucasian, Asian, African American, Hispanic, and other
Gender Values: male, female, and unknown/invalid
Age Grouped in 10-year intervals: 0, 10), 10, 20), …, 90, 100)
Weight Weight in pounds
Admission type Integer identifier corresponding to 9 distinct values, for example, emergency, urgent, elective, newborn, and not available
Discharge disposition Integer identifier corresponding to 29 distinct values, for example, discharged to home, expired, and not available
Admission source Integer identifier corresponding to 21 distinct values, for example, physician referral, emergency room, and transfer from a hospital
Time in hospital Integer number of days between admission and discharge
Payer code Integer identifier corresponding to 23 distinct values, for example, Blue Cross/Blue Shield, Medicare, and self-pay Medical
Medical specialty Integer identifier of a specialty of the admitting physician, corresponding to 84 distinct values, for example, cardiology, internal medicine, family/general practice, and surgeon
Number of lab procedures Number of lab tests performed during the encounter
Number of procedures Numeric Number of procedures (other than lab tests) performed during the encounter
Number of medications Number of distinct generic names administered during the encounter
Number of outpatient visits Number of outpatient visits of the patient in the year preceding the encounter
Number of emergency visits Number of emergency visits of the patient in the year preceding the encounter
Number of inpatient visits Number of inpatient visits of the patient in the year preceding the encounter
Diagnosis 1 The primary diagnosis (coded as first three digits of ICD9); 848 distinct values
Diagnosis 2 Secondary diagnosis (coded as first three digits of ICD9); 923 distinct values
Diagnosis 3 Additional secondary diagnosis (coded as first three digits of ICD9); 954 distinct values
Number of diagnoses Number of diagnoses entered to the system 0%
Glucose serum test result Indicates the range of the result or if the test was not taken. Values: “>200,” “>300,” “normal,” and “none” if not measured
A1c test result Indicates the range of the result or if the test was not taken. Values: “>8” if the result was greater than 8%, “>7” if the result was greater than 7% but less than 8%, “normal” if the result was less than 7%, and “none” if not measured.
Change of medications Indicates if there was a change in diabetic medications (either dosage or generic name). Values: “change” and “no change”
Diabetes medications Indicates if there was any diabetic medication prescribed. Values: “yes” and “no”
24 different kind of medical drugs.
Readmitted Days to inpatient readmission. Values: “0” if the patient was readmitted in less than 30 days, “>30” if the patient was readmitted in more than 30 days, and “No” for no record of readmission
•	Categories in admission type column(admission_type_id)
1: Emergency
2: Urgent
3: Elective
4: New born
5: Not Available
6: NULL
7: Trauma Center
8: Not Mapped
•	Categories in discharge type column(discharge_disposition_id)
1 Discharged to home
2 Discharged/transferred to another short term hospital
3 Discharged/transferred to SNF
4 Discharged/transferred to ICF
5 Discharged/transferred to another type of inpatient care institution
6 Discharged/transferred to home with home health service
7 Left AMA
8 Discharged/transferred to home under care of Home IV provider
9 Admitted as an inpatient to this hospital
10 Neonate discharged to another hospital for neonatal aftercare
11 Expired
12 Still patient or expected to return for outpatient services
13 Hospice / home
14 Hospice / medical facility
15 Discharged/transferred within this institution to Medicare approved swing bed
16 Discharged/transferred/referred another institution for outpatient services
17 Discharged/transferred/referred to this institution for outpatient services
18 NULL
19 Expired at home. Medicaid only, hospice.
20 Expired in a medical facility. Medicaid only, hospice.
21 Expired, place unknown. Medicaid only, hospice.
22 Discharged/transferred to another rehab fac including rehab units of a hospital .
23 Discharged/transferred to a long term care hospital.
24 Discharged/transferred to a nursing facility certified under Medicaid but not certified under Medicare.
25 Not Mapped
26 Unknown/Invalid
30 Discharged/transferred to another Type of Health Care Institution not Defined Elsewhere
27 Discharged/transferred to a federal health care facility.
28 Discharged/transferred/referred to a psychiatric hospital of psychiatric distinct part unit of a hospital
29 Discharged/transferred to a Critical Access Hospital (CAH).

•	Admission source column(admission_source_id)
1 Physician Referral
2 Clinic Referral
3 HMO Referral
4 Transfer from a hospital
5 Transfer from a Skilled Nursing Facility (SNF)
6 Transfer from another health care facility
7 Emergency Room
8 Court/Law Enforcement
9 Not Available
10 Transfer from critial access hospital
11 Normal Delivery
12 Premature Delivery
13 Sick Baby
14 Extramural Birth
15 Not Available
17 NULL
18 Transfer From Another Home Health Agency
19 Readmission to Same Home Health Agency
20 Not Mapped
21 Unknown/Invalid
22 Transfer from hospital inpt/same fac reslt in a sep claim
23 Born inside this hospital
24 Born outside this hospital
25 Transfer from Ambulatory Surgery Center
26 Transfer from Hospice
In payer code and Medical Speciality the missing values are very high so they are not considered generally so the description for each code is not provided
