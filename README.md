# Customer Sign-Up Behaviour & Data Quality Audit

## Project Overview

This project analyses customer sign-up behaviour for Rapid Scale, a SaaS company offering tiered subscription plans. The objective was to perform a data quality audit and generate business insights to support the company’s Monthly Business Review (MBR).

The analysis focuses on identifying data quality issues, understanding user acquisition channels, evaluating subscription plan preferences, and analysing marketing opt-in behaviour across different customer demographics.

---

## Business Problem

Rapid Scale collects customer sign-up data from multiple marketing channels. However, inconsistent and incomplete data can affect the accuracy of business insights.

The Business Intelligence team needed to:

- Identify and resolve data quality issues
- Understand how customers are signing up
- Analyse which plans users prefer
- Evaluate marketing opt-in behaviour
- Generate insights to support marketing and onboarding strategies

---

## Dataset

The primary dataset contains **customer sign-up records**, including:

- customer_id
- signup_date
- acquisition source (Google, Instagram, Referral, etc.)
- region
- subscription plan selected
- marketing opt-in status
- age
- gender

The dataset initially contained **298 records**, which were cleaned to **278 valid records** after removing inconsistent or incomplete entries.

An optional dataset containing **support tickets** was also used to analyse early customer support activity.

---

## Tools & Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Jupyter Notebook

---

## Data Cleaning Process

Several data quality issues were identified and corrected:

- Invalid date values in the `signup_date` column were removed
- Missing `customer_id` values were removed
- Inconsistent plan names such as `basic`, `PRO`, and `PREMIUM` were standardised
- Text values in the age column were converted to numeric values
- Unrealistic ages were treated as missing values
- Missing age values were replaced with the median age
- Missing region values were labelled as **Unknown**
- Inconsistent gender and marketing values were standardised

After cleaning, the dataset was suitable for reliable analysis.

---

## Key Insights

### Subscription Plan Distribution

The Premium plan recorded the highest number of sign-ups, followed closely by the Pro and Basic plans. This indicates that many users are willing to adopt mid-to-high subscription tiers rather than only entry-level pricing.

### Acquisition Sources

Digital channels drive the majority of sign-ups. Video and search-based channels contribute strongly to customer acquisition.

### Customer Demographics

The median customer age is **34**, with most users falling within the **25–40 age group**, suggesting the platform primarily attracts early and mid-career professionals.

---

## Business Question Answers

**1. Which acquisition source brought the most users last month?**  
Google generated the highest number of sign-ups during the most recent month analysed.

**2. Which region shows incomplete data?**  
Several records contained missing region information and were labelled as **Unknown**, indicating incomplete data capture during sign-up.

**3. Are older users more likely to opt in to marketing?**  
Users aged **25–40** show a higher marketing opt-in rate compared with older segments.

**4. Which plan is most commonly selected and by which age group?**  
The Basic plan is most commonly selected among users aged **25–40**, while Premium plans appear slightly more common among older customers.

---

## Stretch Task – Support Activity

The support ticket dataset was merged with the customer sign-up dataset to analyse early support activity.

Results showed that **27 customers contacted support within two weeks of signing up**.

Support activity by plan:

- Pro plan: 12
- Basic plan: 9
- Premium plan: 6

This suggests Pro plan users may require additional onboarding support.

---

## Business Recommendations

1. **Invest in high-performing acquisition channels**  
Search and digital marketing channels generate the majority of new users and should remain a focus for growth strategies.

2. **Improve data collection controls**  
Mandatory fields and dropdown menus should be implemented to reduce missing region and marketing data.

3. **Target the core age segment**  
Marketing campaigns should prioritise the 25–40 age group, which represents the largest portion of customers.

---

## Data Issues Identified

Several data quality risks were discovered during analysis:

- Invalid date formats
- Text values in numeric fields
- Inconsistent category labels
- Missing region information

Implementing automated validation and structured data entry controls would significantly improve data quality.

---


## Author

**Tashmin Hasan**  
Data Analyst  
Skills: Python | SQL | Tableau | Power BI | Excel
