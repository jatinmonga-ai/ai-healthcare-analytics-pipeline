# 🏥 AI-Powered Patient Readmission Analytics Pipeline
Julius AI + Mostly AI + Python | Healthcare Analytics Portfolio Project
Field: Healthcare Analytics | Type: Solo Project | Tools: Julius AI, Mostly AI, Python

# 📌 Overview
An end-to-end healthcare data analytics pipeline built to demonstrate how modern AI tools
can accelerate the data cleaning process by ~80% and enable privacy-safe data augmentation
using synthetic data generation.
Analysed 98,052 real patient records from 130 US hospitals spanning 1999–2008 to
uncover key patterns in 30-day hospital readmission — a real billion-dollar problem for
healthcare systems worldwide.
This is Project 1 of 3 in a Healthcare Analytics Portfolio Series. The same dataset is
also analysed using Excel + Power Query and PostgreSQL.

# 🔧 Tools & Technologies
Tool Purpose: 

1. Julius AI:
AI-assisted data cleaning — ~80% faster than manual 

2. Mostly AI:
Synthetic patient data generation (HIPAA-compliant privacy augmentation)Python — PandasData loading, manipulation, and combining real + synthetic datasets

3. Python — Matplotlib & Seaborn:
All 9 visualizations

4. Jupyter Notebook:
Interactive analysis environment


# 🧹 Data Cleaning — Julius AI
The raw dataset had significant quality issues handled entirely through Julius AI prompts:
1. IssueActionDetail "?" placeholdersReplaced with NaN Across all columns .
2. High-missing columnsDroppedweight (96.9%), max_glu_serum (94.7%), A1Cresult (83.3%), medical_specialty (49.1%), payer_code (39.6%)ID
3. columns Dropped : encounter_id, patient_nbr
4. Zero-variance columns Dropped : examide, citoglipton (100% "No")
5. Near-zero variance Dropped : 7 medication columns (99%+ "No")
6. Age encoding Converted'[0-10)' → 5, '[10-20)' → 15 … '[90-100)' → 95
7. Gender encoding : Converted Male=1, Female=0, dropped Unknown/Invalid
8. Medication encoding Converted: No=0, Steady=1, Up=2, Down=3
9. Target column Created readmitted_binary: '<30'=1, else=0
Result: 101,766 rows → 98,052 clean rows | 50 columns → 31 columns

# 🧬 Synthetic Data — Mostly AI
Generated ~98,052 synthetic patient records using Mostly AI to:

Enable privacy-safe data augmentation aligned with HIPAA principles
Validate that statistical patterns in real data are genuine, not noise
Demonstrate understanding of synthetic data in healthcare contexts

The 4 real vs synthetic comparison charts confirm Mostly AI preserved distributions
across lab procedures, medications, diagnoses, and hospital stay lengths.

# 📊 Key Findings
1. Overall Readmission Rate: Overall Readmission Rate 11.3% of 98,052 patients were readmitted within 30 days
2. Highest Risk Insulin Group : Patients with reduced insulin had a 14% readmission rate vs 10.1% on no insulin
3. Prior Visits Signal: Readmitted patients averaged 1.15 prior inpatient visits vs 0.56 — over 2x more
4. Age Pattern: Readmission rate climbs from 6.7% (age 10-20) to 12% (age 80-90)
5. Synthetic Data Quality : All 4 comparison charts confirm Mostly AI preserved real distributions accurately


# 🚀 How to Run

1. Clone this rep0

2. Install dependencies

3. Open the notebook

4. Run all cells — charts save automatically to /visuals/


# 🎓 Dataset
Name: Diabetes 130-US Hospitals (1999–2008)
Source: UCI Machine Learning Repository
Link: https://archive.ics.uci.edu/dataset/296/diabetes+130-us+hospitals+for+years+1999-2008
Raw Records: 101,766 | After Cleaning: 98,052
Features: 50 raw → 31 after cleaning

# 🏆 Skills Demonstrated

AI-assisted data cleaning workflow using Julius AI (prompt engineering for data tasks)
Synthetic data generation using Mostly AI for privacy-safe analysis
Python data visualisation with Pandas, Matplotlib, and Seaborn
Real vs synthetic data validation and distribution comparison
Healthcare domain knowledge — HIPAA, readmission risk, clinical data patterns


# Part 1 of 3 — Healthcare Analytics Portfolio Series
Project 2: Excel + Power Query | Project 3: PostgreSQL
