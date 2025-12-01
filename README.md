# claims-analysis

# Claims Data Analysis – Stony Brook University Hospital

## Project Overview
This project replicates a real-world workflow commonly performed by healthcare data analysts and revenue cycle teams. Using a sample of prospective claims submitted in **May 2024**, the analysis focuses on identifying billing trends, provider activity, diagnosis and procedure frequency, and payer utilization.  
The goal is to demonstrate how relational claims datasets can be used to support compliance reviews, operational planning, and financial decision-making.

## Data Source
The dataset includes three interconnected claim files:

- **HEADER File** – Claim-level details such as service dates, provider NPIs, and primary payer.
- **LINE File** – Line-level billing information including CPT/HCPCS codes, units, modifiers, and charges.
- **CODE File** – ICD-10 diagnosis codes mapped to each claim.

These files form a relational structure linked by **ProspectiveClaimId**.

## Repository Structure


## How to Run the Notebook

### 1. Clone the Repository
```bash
git clone <your-repository-url>
cd claims-analysis

# Install Dependencies
pip install -r requirements.txt

# Run analysis
notebooks/claims_analysis.ipynb
```
# Key Findings
1. Provider Billing Activity

A small group of billing providers account for a large portion of total claim volume.
The top provider billed significantly more claims than others, suggesting higher patient throughput or specialized service patterns.

2. Payer Mix Insights

Medicare and other major payers represent a substantial share of total claims.
Understanding payer distribution can help guide contract management and reimbursement planning.

3. Common Diagnoses

Diagnosis frequencies highlight recurring clinical themes in the dataset.
Multiple high-volume ICD-10 codes relate to musculoskeletal conditions, routine follow-ups, and other commonly treated issues.

4. Procedure Utilization

Frequently billed CPT/HCPCS codes correspond to standard evaluation, management, and routine outpatient procedures.

5. Complexity Indicators

By examining the number of diagnosis codes per claim, several providers appear to manage more clinically complex cases, indicating potential specialization or higher-acuity patient populations.

# Required Libraries
```
pandas >= 1.5.0
matplotlib >= 3.6.0
seaborn >= 0.12.0
jupyter >= 1.0.0
```
