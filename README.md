# 🏥 Analysing NHS Primary Care Appointment Capacity and Utilisation
Exploratory data analysis project using Python (pandas, NumPy, Matplotlib, Seaborn) to clean, prepare, analyse, and visualise insights into national and regional appointment demand, capacity utilisation, and “did not attend” (DNA) rates across NHS primary care.

---

## 📌 Executive Summary
This project analyses NHS primary care appointment data to determine whether national and regional capacity was adequate, how effectively resources were utilised, and where systemic pressures or inefficiencies occurred. The analysis covers August 2021 to June 2022 and focuses on demand vs. capacity, utilisation rates, appointment mode preferences, and DNA patterns. The findings indicate that although monthly national demand remained below capacity, daily demand exceeded manageable levels more than half the time, several Integrated Care Boards (ICBs) consistently lacked sufficient capacity, and DNA rates contributed to avoidable wastage. Based on these insights, the project recommends shifting remote and virtual appointment demand from pressured ICBs to neighbouring ICBs with unutilised capacity, and piloting an overbooking policy for appointment modes with consistently high DNA rates to reduce wasted capacity.

---

## 📁 Project Files
- `actual_duration.csv` — Original dataset
- `appointments_regional.csv` — Original dataset (zipped due to size)
- `national_categories.csv` — Original dataset (zipped due to size)
- `tweets.csv` — Original dataset
- `Python Script.ipynb` — Code for analysis and visualisations for stakeholder presentation
- `Technical Report and Insights.pdf` — Business problem, assumptions / limitations, data wrangling and analysis, and recommendations

---

## ❓ Business Problem / Opportunity
The NHS is considering expanding its primary care service capacity to meet the needs of its patients. However, it must first understand how well its existing capacity is being utilised before deciding whether to increase this or focus on making better use of existing resources and infrastructure.

The two high‑level business questions are:

  1. Has there been adequate staff and capacity?
  2. What was the actual utilisation of resources?

This project uses internal NHS datasets to assess national and regional demand, capacity utilisation, appointment mode patterns, and DNA rates.

---

## 🔬 Methodology
- Imported and inspected datasets using pandas
- Validated data using a custom inspect_and_validate_data() function
- Removed duplicated rows from the regional dataset
- Performed outlier analysis and retained legitimate variations
- Calculated national monthly demand vs. capacity
- Estimated daily demand to identify manageable vs. unmanageable days
- Identified ICBs with insufficient capacity and neighbouring ICBs with unutilised capacity
- Mapped ICB names across datasets to analyse remote / virtual appointment demand
- Calculated national and regional appointment utilisation rates
- Calculated DNA rates overall and by appointment mode
- Created exploratory and explanatory visualisations using Matplotlib and Seaborn

---

## 🛠️ Tools and Skills Used
- Python: pandas, NumPy, Matplotlib, Seaborn
- Jupyter Notebook: Data exploration and analysis
- Data Wrangling: Grouping, filtering, merging, mapping, and custom functions
- Data Visualisation: Timeseries charts, bar charts, stacked bar charts, and tables
- Analytical Skills: Capacity modelling, utilisation analysis, DNA rate analysis

---

## 📊 Insights

### National Demand vs. Capacity

Monthly demand remained below the estimated national capacity of 36 million appointments.

<img width="1004" height="567" alt="image" src="https://github.com/user-attachments/assets/4d86ee0a-31ab-46a7-9cfb-7db77b71e39f" />

However, daily demand was manageable on only 47.6% of observed days, indicating that capacity pressures occurred frequently.

<img width="1004" height="567" alt="image" src="https://github.com/user-attachments/assets/35d9f9c3-ce4a-4a67-95bc-daec78556d12" />

---

### Regional Capacity Issues

Several ICBs consistently lacked sufficient capacity.

<img width="1004" height="567" alt="image" src="https://github.com/user-attachments/assets/aa4b8ff1-5d9e-45bd-a199-0653daeb3645" />

Neighbouring ICBs often had unutilised appointments, suggesting opportunities for redistributing demand or improving cross‑ICB coordination.

<img width="1004" height="567" alt="image" src="https://github.com/user-attachments/assets/5374d071-1c4d-497a-92ea-e47ed306b9f3" />

---

### Remote / Virtual Appointment Demand

Six ICBs experienced demand for 10–14 million remote / virtual appointments, highlighting significant variation in appointment mode preferences across regions.

<img width="1004" height="567" alt="image" src="https://github.com/user-attachments/assets/32b2fb3b-3605-4508-add6-649620d6b5eb" />

---

### Capacity Utilisation

The NHS used 74% of its total national capacity.

<img width="1004" height="567" alt="image" src="https://github.com/user-attachments/assets/54826b78-6f76-45d1-a118-84b52a446a3e" />

North East and North Cumbria ICB’s demand exceeded its capacity by 77%, indicating persistent regional strain.

<img width="1004" height="567" alt="image" src="https://github.com/user-attachments/assets/ed5bcf86-657e-448e-b7a9-e6e06fa23244" />

---

### DNA Rates

DNA rates were comparable nationally and regionally.

<img width="1004" height="567" alt="image" src="https://github.com/user-attachments/assets/223b81ab-78b7-491f-b464-890ea66aae22" />

<img width="1004" height="567" alt="image" src="https://github.com/user-attachments/assets/1f4644a3-92df-4266-b275-2b6630bccf85" />

Approximately 5% of face‑to‑face and video / online appointments were DNAs in North East and North Cumbria.

<img width="1004" height="567" alt="image" src="https://github.com/user-attachments/assets/7cf03fd1-96f8-4e19-a7ad-3f1d0257869d" />

Month‑on‑month analysis showed the lowest DNA rates were 4.81% (face‑to‑face) and 3.78% (video / online).

<img width="1004" height="567" alt="image" src="https://github.com/user-attachments/assets/d54a3eac-fc64-45ab-bdc7-888ff5c51906" />

---

### Social Media (X / Twitter) Analysis

Sixteen relevant hashtags appeared more than ten times each, featuring in 18% of sampled tweets, indicating moderate public engagement with primary care topics.

<img width="1004" height="567" alt="image" src="https://github.com/user-attachments/assets/86e39187-bec0-4e81-9cdd-a823e9a93b3f" />

---

## 🎯 Recommendations

Investigate opportunities to redistribute demand from high‑pressure ICBs to neighbouring areas with unutilised capacity.

Explore overbooking strategies for appointment modes with consistently high DNA rates to reduce wasted capacity.

Repeat this analysis after the financial year 2026/27, once new geographic boundaries have been in place for a full year.

Incorporate funding or population data to more accurately assess each ICB’s available capacity.

Include workforce data (e.g., National Workforce Reporting System, Additional Roles Reimbursement Scheme) to determine whether staffing levels are adequate.
