# Credit Card Weekly Status Report

### Dashboard Link : https://app.powerbi.com/view?r=eyJrIjoiYjY2ZjQ2NjktZTg3Mi00ODU5LTlkMTEtYjJjOGU5YTE0NWZiIiwidCI6IjI3ZDllYmQwLWYyZjktNGFhMy1iNmY5LWM2ZDAzODI4NjEyNyJ9&pageName=ba17a14f0effee652289

## Problem Statement

To develop a comprehensive & Interactive credit
card weekly dashboard that
provides real-time insights into key
performance metrics and trends,
enabling stakeholders to monitor
and analyze credit card operations
effectively.


### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a csv file.
- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Step 3 : Also since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset".
- Step 4 : It was observed that in one of the columns errors & wrong date formats were present.
- Step 5 : changed the formatting of the "week_start_date" to mm/dd/yy from dd/mm/yy after it was observed there was still a errorbecause some of the dates were wrongly written so it was chanded to random dates between the selected dates
- Step 6 : In the report view, under the view tab, theme was selected.
- Step 7 : Appropriate title was given using the text box 
- Step 9 : Three card visuals were added to the canvas, one representing sum of revenue & other representing total transaction amt, total intrest earned and total transactions.
           Using visual level filter from the filters pane, basic filtering was used 
           
          All visuals are based on the revenue generated during the period.
- Step 10 : A line and stacked column chart was also added to the report design area representing the Sum of revenue and transaction amt by quarter . 

## Dax Queries used
for creating new columns following DAX expression was written;
 ### 1. Age group
       
       AgeGroup = SWITCH
    (
    TRUE(),
    'public cust_detail'[customer_age] < 30, "20-30",
    'public cust_detail'[customer_age] >= 30 && 'public cust_detail'[customer_age] < 40, "30-40",
    'public cust_detail'[customer_age] >= 40 && 'public cust_detail'[customer_age] < 50, "40-50",
    'public cust_detail'[customer_age] >= 50 && 'public cust_detail'[customer_age] < 60, "50-60",
    'public cust_detail'[customer_age] >= 60, "60+",
    "unknown"
    )
### 2. Income group
    IncomeGroup = SWITCH
    (
    TRUE(),
    'public cust_detail'[income] < 35000, "Low",
    'public cust_detail'[income] >= 35000 && 'public cust_detail'[income] <70000, "Med",
    'public cust_detail'[income] >= 70000, "High",
    "unknown"
    )
### 3. week number 
    week_num2 = WEEKNUM('public cc_detail'[week_start_date])
### 4. Revenue 
    Revenue = 'public cc_detail'[annual_fees] + 'public cc_detail'[total_trans_amt] + 'public cc_detail'[interest_earned]
- Step 15 : Following new measures were created 
### 1. Current week revenue
    Current_week_Reveneue = CALCULATE(
        SUM('public cc_detail'[Revenue]),
        FILTER(
            ALL('public cc_detail'),'public cc_detail'[week_num2] = MAX('public cc_detail'[week_num2])))
### 2. Previous week revenue 
 Current_week_Reveneue = CALCULATE(
    SUM('public cc_detail'[Revenue]),
    FILTER( ALL('public cc_detail'),
    'public cc_detail'[week_num2] = MAX('public cc_detail'[week_num2])))


 - Step 18 : The report was then published to Power BI Service.
 
 
# Snapshot of credit card transaction report (Power BI Service)

![dashboard image ](https://github.com/user-attachments/assets/c9237ca6-79e0-4dae-a52b-6b66d26e4450)


 # Snapshot of credit card Customer report


![dashboard img 2](https://github.com/user-attachments/assets/13ca3aae-828c-42c1-acdf-1fa9fd9068d8)

# Insights
- Project Insights- Week 53 (31st Dec)
- WoW change:
- Revenue increased by 28.8%,
- Total Transaction Amt & Count increased by xx% & xx%
- Customer count increased by xx%
- Overview YTD:
- Overall revenue is 57M
- Total interest is 8M
- Total transaction amount is 46M
- Male customers are contributing more in revenue 31M, female 26M
- Blue & Silver credit card are contributing to 93% of overall transactions
- TX, NY & CA is contributing to 68%
- Overall Activation rate is 57.5%
- Overall Delinquent rate is 6.06%
