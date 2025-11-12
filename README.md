# 🏨 Hotel Operations Analysis (LuxurStay Hotels)

Goal: Investigate the root causes of slow room service and identify hotel branches with the lowest customer satisfaction.

## 📘 Background

LuxurStay Hotels is an international hotel chain catering to both business and leisure travelers.
Recently, management noticed an increase in complaints about slow room service, which caused the customer satisfaction rating to drop below their 4.5 target.

You’ve been asked to collaborate with the Head of Operations to analyze data, pinpoint operational inefficiencies, and identify which hotel branches and services need the most improvement.

## 🗂️ Dataset Overview

You’ve been given a hotel operations database containing several tables, including:

Table	Description
branch	Hotel branch details such as ID, location, and region
service	Different services provided (e.g., Meal, Laundry, Room Service)
request	Customer service requests and duration times
feedback	Customer ratings linked to branches and services

⚙️ You only have data where customers provided feedback ratings.

## 🧠 Project Tasks & SQL Logic
### 🧩 Task 1 — Data Validation and Cleaning

Before analysis, confirm that the data in the branch table matches the description provided by the data team.
Identify invalid entries (e.g., incorrect IDs, null values, misspelled regions) and clean them.

✅ Goal:
Return a cleaned version of the branch data as a DataFrame named:

clean_branch_data


### ⏱️ Task 2 — Response Time Analysis

Management suspects certain branches are slower in responding to customer requests.

✅ Goal:
Calculate the average and maximum time taken to respond to a request for each service and branch.

🧾 Expected Output Columns:

service_id

branch_id

avg_time_taken

max_time_taken

🧮 Round values to 2 decimal places


### 🍽️ Task 3 — Target Improvement Areas (EMEA + LATAM)

The management wants to improve Meal and Laundry services in the EMEA and LATAM regions.

✅ Goal:
Return relevant service descriptions, branch info, request IDs, and ratings.

🧾 Expected Output Columns:

service_description

branch_id

branch_location

request_id

rating

### ⭐ Task 4 — Identify Underperforming Hotels

To focus on problem areas, identify services and branches where the average rating < 4.5.

✅ Goal:
Return branch-service combinations below the management’s satisfaction target.

🧾 Expected Output Columns:

service_id

branch_id

avg_rating


## 🧰 Tools & Technologies
Tool	Purpose
PostgreSQL / SQL	Data extraction and analysis
Python (pandas, psycopg2)	Connecting and transforming SQL outputs
Jupyter Notebook	Query documentation and result visualization
## 📈 Insights & Potential Findings

Branches with invalid data were identified and corrected to ensure clean analysis.

Response time varied significantly across services — Meal Service showed the highest delay in EMEA.

LATAM branches had consistent issues in Laundry service, correlating with low ratings.

Several branch-service pairs averaged below 4.5, pinpointing areas for staff retraining and process review.

## 🏁 Next Steps

Automate monthly SQL reports to monitor average ratings and response times.

Build an interactive Power BI dashboard for hotel management to visualize service efficiency.

Recommend process optimization for Meal and Laundry workflows in EMEA and LATAM.

check my SQL Associate certificate:https://www.datacamp.com/certificate/SQA0018992446719
