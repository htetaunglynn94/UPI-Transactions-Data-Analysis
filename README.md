# 📊 UPI Transactions Data Analysis (Power BI Project)

## Project Overview

This project analyzes **UPI (Unified Payments Interface) transaction data** to evaluate transaction behavior, system performance, and user adoption patterns across different demographics and regions.

The objective is to identify **usage trends**, detect **transaction inefficiencies**, and uncover **data-driven insights** that can support improvements in digital payment systems.

**PowerBI Report**: [UPI Transactions Data Analysis.pbix](https://app.powerbi.com/links/Y6OOuUsY68?ctid=35ae1710-01c9-4681-aee5-aefcb73885b1&pbi_source=linkShare&bookmarkGuid=af2b3df3-2332-458d-a522-c3197b28b841)

---

## Objectives

🔹 Enable interactive filtering across multiple dimensions (Bank, City, Device, Gender, etc.)  
🔹 Analyze transaction patterns by:

  * Transaction Type
  * Payment Method
  * Merchant
  * Purpose

🔹 Evaluate transaction success vs failure rates  
🔹 Segment users by **Age Group and Gender**  
🔹 Identify high-usage regions and behavioral trends  
🔹 Provide actionable insights for improving transaction efficiency

---

## Dataset Information

* The information in dataset is recorded in 2024
* Dataset: [UPI_Transactions.xlsx](https://github.com/user-attachments/files/26998057/UPI_Transactions.xlsx)

---

## Report Structure

### Overview Page

* 10 synchronized slicers across report pages
* 2 Line Charts
* 2 Column Charts
* Bookmark Navigator (4 views for dynamic chart switching)

### Matrix Page

* 10 synchronized slicers
* Matrix table with conditional formatting for enhanced readability

### Insights Page

* Clustered Column Chart
* Stacked Column Charts (2)
* Donut Chart
* Bar Chart

---

## Data Processing Steps

### 1️⃣ Data Loading

* Imported dataset into Power BI
* Split `TransactionTime` into separate **Date** and **Time** columns using delimiter
* Verified and corrected data types and formats
* Applied transformations

---

### 2️⃣ Data Preprocessing

#### 🔹 Age Group Segmentation

Customer age was categorized using DAX:

| Age Range | Group | Ratio |
| --------- | ----- | ----- |
| ≤ 30      | A1    | 27.5% |
| ≤ 40      | A2    | 25.0% |
| > 40      | A3    | 47.5% |

```DAX
Age Groups = 
IF('UPI Transactions'[CustomerAge] <= 30, "A1",
    IF('UPI Transactions'[CustomerAge] <= 40, "A2", "A3"))
```

---

#### 🔹 Slicers Configuration

Implemented and synchronized 10 slicers for dynamic filtering:

* Bank Name (Sender & Receiver)
* City
* Device Type
* Gender
* Age Group
* Merchant Name
* Payment Method
* Purpose
* Transaction Type

---

## Data Visualization & Analysis

### Overview Page

* Interactive charts controlled by slicers
* Bookmark navigator allows switching between multiple chart views in the same space
* Enables efficient comparison of transaction patterns

---

### Matrix Page

* Displays detailed transaction breakdown
* Conditional formatting highlights key trends and anomalies
* Fully interactive via slicers

---

### Insights Page (Key Findings)

#### User Behavior

* Customers aged **> 40 (A3 group)** represent the **highest transaction usage**, indicating strong adoption among older users
* Younger users (A1 group ≤ 30) show high activity in **shopping-related transactions**

---

#### Transaction Performance

* A noticeable proportion of transactions are marked as **Failed**, particularly in:

  * **Shopping transactions**
  * Specific merchants such as **Flipkart**

👉 This may indicate:

* Payment gateway issues
* Merchant-side processing limitations
* Network or authentication failures

---

#### Regional Trends

* **Mumbai and Delhi** are the leading cities in transaction volume  
  👉 Reflecting higher digital payment adoption in metropolitan areas

---

#### Behavioral Patterns

* Device type and payment method influence transaction success rates
* Shopping remains one of the most dominant transaction purposes across segments

---

## Conclusion

This analysis demonstrates that UPI transactions are widely adopted across all age groups, with particularly strong engagement from users aged above 40. Urban centers such as Mumbai and Delhi dominate transaction activity, highlighting the role of infrastructure and digital awareness in driving adoption.

However, the presence of frequent **failed transactions**, especially in shopping-related use cases and specific merchants, indicates potential inefficiencies within the payment ecosystem. These issues may stem from technical limitations, system reliability, or integration challenges between banks and merchants.

To enhance overall performance and user experience, it is recommended to:

* Improve transaction reliability and reduce failure rates
* Strengthen integration between payment systems and merchants
* Optimize user experience in high-frequency transaction categories such as shopping

Overall, the insights from this analysis provide valuable direction for improving **digital payment efficiency, user satisfaction, and system robustness**.

---

## Tools Used

* Power BI (Data Visualization & Dashboarding)
* Excel (Data Source)

---

## Contact

If you have feedback or opportunities, feel free to connect:

* [LinkedIn](https://www.linkedin.com/in/htet-aung-lynn-64ba06146/)
* [GitHub](https://github.com/htetaunglynn94)

---
