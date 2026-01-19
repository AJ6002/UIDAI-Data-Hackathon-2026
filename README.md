# UIDAI Aadhaar Data Analysis & Anomaly Detection

## 📌 Project Overview
This project analyzes **UIDAI Aadhaar enrolment, demographic update, and biometric update datasets** to uncover operational patterns, regional imbalances, and potential data quality anomalies.

Instead of limiting the analysis to basic enrolment counts, the project focuses on **interactions between datasets** to identify districts where Aadhaar **update activity is disproportionately high relative to new enrolments**, indicating possible administrative stress, data entry issues, or infrastructure inefficiencies.

This work was developed as part of the **UIDAI Data Hackathon**.

---

## 🎯 Problem Statement
**How can UIDAI identify regions where Aadhaar update activity is abnormally high relative to new enrolments, and what do these patterns reveal about operational stress, data quality, or administrative inefficiencies at state and district levels?**

---

## 🗂️ Datasets Used
All datasets are **official UIDAI aggregated datasets**:

1. **Aadhaar Enrolment Dataset**
   - New enrolments by date, state, district, PIN code
   - Age-wise categories (0–5, 5–17, 18+)

2. **Aadhaar Demographic Update Dataset**
   - Updates related to name, address, DOB, gender, mobile
   - Aggregated by geography and time

3. **Aadhaar Biometric Update Dataset**
   - Fingerprint, iris, face updates
   - Particularly relevant for child-to-adult transitions

📌 **No external datasets were used**, as per hackathon guidelines.

---

## 🧠 Methodology
The analysis follows a **structured, governance-oriented pipeline**:

1. **Data Understanding & Cleaning**
   - Merged multiple CSV chunks
   - Standardized state and district names
   - Handled inconsistencies and formatting issues

2. **Exploratory Data Analysis (EDA)**
   - National and state-level enrolment trends
   - Age-wise enrolment distribution
   - Temporal “Aadhaar Pulse” analysis
   - Comparative state rankings

3. **Feature Engineering**
   - Constructed **Update Pressure Ratio**  
     *(Total Updates ÷ Total Enrolments)* at district level

4. **Anomaly Detection**
   - Identified districts with unusually high update pressure
   - Used statistical thresholding (Z-score based logic)

5. **Interpretation & Governance Insights**
   - Translated technical findings into administrative implications

---

## 📊 Key Visualizations
The project includes:
- State-wise enrolment & update bar charts  
- Age-wise enrolment distribution  
- Daily Aadhaar enrolment pulse (time series)  
- Enrolment vs Update bubble charts  
- District-level update pressure distribution  
- Highlighted high-pressure districts  

📌 **Only the most relevant visuals are included in the final PDF** to maintain clarity.

---

## 🔍 Key Insights
- Certain districts exhibit **extremely high update-to-enrolment ratios**
- Update activity does not scale linearly with enrolment volume
- Biometric updates show higher volatility than demographic updates
- District-level analysis reveals patterns hidden at the state level

---

## 🏛️ Administrative & Policy Implications
- Early detection of **data quality issues**
- Targeted training for enrolment operators
- Optimized resource allocation
- Evidence-based monitoring of Aadhaar infrastructure stress

---

## ⚠️ Limitations & Ethics
- Analysis is based on **aggregated data only**
- No individual-level tracking or identification
- Results indicate **signals**, not confirmed fraud
- Designed strictly for **policy improvement**, not enforcement

---

## 🧰 Tech Stack
- **Python**
- Pandas, NumPy
- Plotly, Matplotlib, Seaborn
- Jupyter Notebook

---


## ▶️ How to Run
1. Clone the repository  
2. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn plotly
3.jupyter notebook
## ⚖️ License
This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.
