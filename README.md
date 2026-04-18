# capstone_dx_prediction
Predicting next-visit diagnoses using EHR data — MIMIC-IV

**Author:** Aaliyah Vincent  
**Capstone Mentor:** Dr. Boubakari Ibrahimou & Henry Jartu  
**Track:** Biostatistics Data Analytics

---

## Overview
This project builds a custom neural network (DxTabNet) trained on 100,101 
patients from the MIMIC-IV EHR database to predict which diagnoses a patient 
is most likely to receive at their next hospital visit, based entirely on their 
prior admission history. The model achieves Hits@20 = 0.927 across a 
vocabulary of 27,205 possible diagnoses.

---

## Data Access
This project uses the **MIMIC-IV** dataset (v3.1), developed by the MIT 
Laboratory for Computational Physiology and hosted on PhysioNet.

**The raw data cannot be shared** as it requires completion of a credentialed 
data use agreement due to patient privacy protections.

To access the data yourself:
1. Create an account at [physionet.org](https://physionet.org)
2. Complete the required CITI training course
3. Apply for credentialed access to MIMIC-IV
4. Once approved, download from: https://physionet.org/content/mimiciv/3.1/

---

## Project Structure
Notebooks:
01_data_exploration.ipynb         # Initial data loading, LOS analysis, early merges
02_data_preparation.ipynb     # Covers both merging AND the heart failure EDA setup
03_mimic_dx_prediction_sparse1.ipynb  # Feature building, multi-label architecture setup and evaluation functions
04_mimic_dx_prediction_sparse_with_clustering.ipynb        # DxTabNet, training, Top-K eval, clustering
---

## How to Reproduce
1. Obtain MIMIC-IV access (see above)
2. Clone this repository
3. Install dependencies: `pip install -r requirements.txt`
4. Place your MIMIC-IV files in a `/data` folder
5. Run notebooks in order (01 → 04)

---

## Key Results
| Metric | Score |
|--------|-------|
| Hits@20 | 0.927 |
| Hits@10 | 0.886 |
| Hits@5  | 0.821 |
| F1 Micro | 0.2396 |
| Recall Micro | 0.2971 |

---

## Requirements
See `requirements.txt`

---

## Project Website
[View full project summary ->](WEBSITE LINK HERE)
