 
Global AML Data Analysis Review with Power BI


The Global Anti-Money Laundering Review dashboard provides an interactive overview of customer risk and lottery-related transaction activity. It combines transaction amounts, sources of funds, countries, and risk ratings to help office employees, compliance officers, and managers explore patterns and identify records that require further review. The dashboard includes comparisons by funding source and country, a breakdown of customer records by risk rating, and detailed transaction tables to support closer examination.

A.Goal of Powerbi Dashboard
The dashboard’s purpose is to make AML and Know Your Customer (KYC) data easier to understand and use. By organizing information into clear visual summaries and supporting tables, it helps users prioritize reviews and make informed decisions. Risk ratings should be treated as indicators for investigation, rather than proof of money laundering.

B.Data Preparation

Before creating or interpreting the visualizations, I extracted the dummy data from Google. I completed the following preparation steps to ensure the data is accurate, consistent, and appropriately protected.

 1. Validate customer and transaction identifiers

Check that `CustomerID` and `TransactionID` are complete and investigate duplicate records. Each customer should have a consistent identifier, while each transaction should have a unique identifier. A `CustomerID` may legitimately appear more than once when a customer has multiple transactions; these records should not automatically be removed.

 2. Assign the correct data types

Ensure that:

- `DOB` and `TransactionDate` are stored as date fields.
- `TransactionAmount` is stored as a decimal or fixed-decimal numeric field.
- `RiskScore` is stored as a numeric field.
- Customer and transaction identifiers retain their original formatting.

Invalid dates, missing amounts, and unexpected risk-score values should be flagged for review before analysis.

 3. Standardize category labels

Use consistent spelling and formatting for country names, sources of funds, and transaction types. Remove unnecessary spaces and resolve inconsistent labels so that the same category does not appear as several separate groups in the dashboard.

 4. Protect sensitive customer information

Restrict access to names, addresses, and dates of birth. Summary dashboard pages should display only the customer information necessary for their intended audience, while identifiable records should be limited to authorized staff.

 5. Define risk bands and transaction thresholds

Agree on risk-band boundaries and the definition of a high-value transaction before building charts. Create a derived **Risk Band** field to group scores into low-, medium-, and high-risk categories.

The boundaries should follow the organization’s approved policy and be applied consistently across charts, tables, and filters. The displayed dashboard already uses these three risk categories, making consistent classification particularly important. [ppl-ai-file-upload.s3.amazonaws](https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/images/135666848/04f3b0b2-80d1-48bd-a745-177b7da295c0/AML-Data-Analysis.jpg)

 6. Validate dashboard calculations

Before publication, reconcile dashboard totals with the prepared dataset. Clearly distinguish between transaction counts and distinct customer counts, and confirm that filters produce the expected results. Use clearly defined risk measures so viewers understand what each visual represents.

 Intended Outcome

With these preparation steps completed, the dashboard can serve as a clear, reliable review tool—helping employees understand risk patterns, compare transaction activity, and identify where further investigation is needed while protecting customer information.

ower BI Project 
https://github.com/sonaljay28/AML-Data-Analysis/blob/main/AML%20Data%20Analysis.png






https://github.com/sonaljay28/AML-Data-Analysis/blob/main/AML%20Data%20Analysis.png
