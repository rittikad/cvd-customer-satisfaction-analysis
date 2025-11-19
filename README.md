# 📊 Public Health & Retail Analytics – Dual Statistical Analysis Project

[![R](https://img.shields.io/badge/Language-R-blue)](https://www.r-project.org/) [![tidyverse](https://img.shields.io/badge/Library-tidyverse-orange)](https://www.tidyverse.org/) [![ggplot2](https://img.shields.io/badge/Visualization-ggplot2-green)](https://ggplot2.tidyverse.org/)

---

## 🚀 Project Overview

This project combines **public health** and **retail analytics** to deliver **data-driven insights** across two domains:

1. **Cardiovascular Disease (CVD) Analysis** – Identify key factors influencing CVD prevalence across English local authorities.  
2. **Retail Customer Satisfaction Analysis** – Understand store-level drivers of customer satisfaction, including delivery time and staff morale.  

**Key Achievements:**  
- Identified **poverty as the strongest predictor** of CVD, guiding potential public health interventions.  
- Discovered that **delivery time significantly affects satisfaction**, especially in high SES stores.  
- Demonstrated ability to **translate statistical analysis into actionable business and policy recommendations**.

---

## 🎯 Business Objectives

### 🩺 Public Health (CVD Analysis)
- Identify **lifestyle & demographic factors** driving CVD prevalence.  
- Provide **evidence-based insights** for policymaking, resource allocation, and public health strategies.

### 🏪 Retail (Customer Satisfaction Analysis)
- Determine **store-level factors** impacting customer satisfaction.  
- Analyze **delivery time effects by socio-economic context**.  
- Offer actionable recommendations for **operational improvements and customer experience**.

---

## 📂 Dataset & Scope

<details>
<summary>Click to expand dataset details</summary>

### 1. CVD Dataset (England Local Authorities)
- **Source:** UK Office for National Statistics  
- **Observations:** Each row = one local authority  
- **Variables:**
  - `%CVD` – Cardiovascular disease prevalence  
  - `%Overweight` – Adults overweight  
  - `%Poverty` – Residents in poverty  
  - `%Smokers` – Smoking prevalence  
  - `WellbeingScore` – Average wellbeing  
  - `Population` – Total population  

### 2. Retail Customer Satisfaction Dataset
- **Observations:** Each row = one retail store  
- **Variables:**
  - `CustomerSatisfaction` – Average rating  
  - `StaffSatisfaction` – Employee morale  
  - `DeliveryTime` – Avg delivery time  
  - `NewProductRange` – Launch of new products (Yes/No)  
  - `SES` – Socio-economic classification: Low/Medium/High  

</details>

---

## 🛠 Methodology

<details>
<summary>Click to expand methodology details</summary>

### 1. Data Cleaning & Quality Checks
- Verified **missing values**, duplicates, and structural consistency  
- Ensured **numeric variables correctly typed** for modelling  
- Retained outliers when they reflected **true population differences**

### 2. Descriptive Analysis
- Calculated **means, standard deviations, and ranges**  
- Explored **distributions** to understand variability  
- Identified potential predictors for regression models

### 3. Statistical Modelling

#### 🩺 CVD Analysis
- **Multiple Linear Regression:** `%CVD ~ %Overweight + %Poverty + %Smokers + WellbeingScore`  
- Evaluated **coefficients, p-values, confidence intervals**

#### 🏪 Retail Analysis
- **Multiple Linear Regression:** `CustomerSatisfaction ~ StaffSatisfaction + DeliveryTime + SES + NewProductRange + DeliveryTime:SES`  
- Interaction term `DeliveryTime × SES` to identify differences across socio-economic contexts

### 4. Visualization
- **CVD:** Effect plot showing Poverty → CVD  
- **Retail:** Interaction plot showing DeliveryTime × SES effects  
- Used ggplot2 for **clear, interpretable charts**  

</details>

---

## 📈 Results & Insights

### 🩺 CVD Analysis
| Predictor | Effect on CVD | Significance | Summary |
|-----------|---------------|-------------|---------|
| Poverty   | Strong ↑      | Highly sig. | Poverty is the dominant predictor of CVD across local authorities |
| Overweight| Moderate ↑    | Significant | Overweight population contributes to higher CVD prevalence |
| Smoking   | Small ↑       | Moderate    | Smoking has a limited effect after controlling for poverty |
| Wellbeing | ↓             | Weak        | Higher wellbeing slightly reduces CVD prevalence |

### 🏪 Retail Analysis
| Factor | Effect on Satisfaction | Significance | Summary |
|--------|----------------------|-------------|---------|
| DeliveryTime | Strong ↓ | Highly sig. | Faster delivery improves customer satisfaction; high SES stores are most sensitive |
| StaffSatisfaction | ↑ | Significant | Happier staff positively influences customer satisfaction |
| NewProductRange | ~0 | Not sig. | Product launches do not significantly affect satisfaction |
| SES | Varied | Significant | Baseline satisfaction varies across socio-economic contexts |
| DeliveryTime × SES | Strong interaction | Significant | High SES stores penalize slow delivery more strongly |

---

## 📝 Recommendations

### 🩺 Public Health
- Prioritize **poverty reduction programs** for long-term health impact  
- Combine socio-economic interventions with **lifestyle health programs**  
- Use wellbeing indicators to identify regions needing **mental and physical support**

### 🏪 Retail Strategy
- Reduce **delivery times**, especially for high SES stores  
- Strengthen **employee wellbeing programs** to boost customer satisfaction  
- Optimize **logistics and delivery management** for premium locations  
- Avoid relying solely on **new product launches** to improve satisfaction  

---

## 🌟 Business & Analytical Impact
- **Policy Relevance:** CVD insights inform government and public health decision-making  
- **Operational Improvement:** Retail findings guide logistics, staffing, and customer experience  
- **Customer Experience:** Delivery-time sensitivity insights allow targeted interventions across SES levels  

---

## 💡 Skills Demonstrated
- **Programming & Tools:** R, tidyverse, ggplot2  
- **Statistical Techniques:** Regression, interaction effects, hypothesis testing  
- **Data Analysis:** Cleaning, exploring, summarizing, interpreting  
- **Visualization:** Effect plots, interaction plots  
- **Business Analytics:** Translating statistical results into actionable recommendations  
- **Reporting:** Communicating complex results to technical and non-technical stakeholders  

---

## 📁 Repository Contents
- `Code` – Statistical Modelling + interaction analysis for both analyses  
- `HTML_Report` – Full rendered report with visualizations  
- `Data/` – Raw data for both analyses  
- `README.md` – Project documentation  

---

**💡 Outcome:**  
This dual-analysis project provides **actionable insights** for both public health and retail contexts. It demonstrates the ability to apply **rigorous statistical methods** and present findings in a way that drives **policy and business decisions**.
