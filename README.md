# amitdubli_2511380_part2_kpi_experiment
Part 2: KPI Framework, Business Experiment Analysis &amp; Decision Recommendation

# Task 1: Business Problem Statement

### Business Objective

Evaluate whether the new onboarding and activation campaign should replace the existing onboarding experience for all new users.

### Decision to be Made

* Determine whether the **Treatment** onboarding experience performs better than the **Control** onboarding experience.
* Decide whether the new onboarding campaign should be rolled out to all users.

### Who the Decision Impacts

* Executive Leadership (business strategy and revenue growth)
* Product Team (onboarding experience)
* Marketing Team (campaign effectiveness)
* Customer Success Team (support workload)
* New Users (overall onboarding experience)

### Success Metrics (Primary KPIs)

The new onboarding campaign should improve:

* Trial Start Rate
* Onboarding Completion Rate
* **Paid Conversion Rate (Primary Success Metric)**
* Average Revenue per User (ARPU)
* User Engagement Score
* Average Days to Convert (lower is better)

### Risks to be Monitored (Guardrail Metrics)

The new onboarding experience should **not** negatively impact customer experience. The following guardrail metrics will be monitored:

* Increase in Support Tickets
* Increase in Refund Requests
* Longer Time to Convert
* Decrease in User Engagement
* Reduction in Revenue

### Evidence Required Before Recommendation

A recommendation to launch the new onboarding campaign will be made only if:

* The Treatment group shows a higher Paid Conversion Rate than the Control group.
* Revenue and user engagement improve.
* Guardrail metrics remain stable or improve.
* The observed improvements are statistically significant.
* Performance is consistent across key user segments such as Region, Device Type, Traffic Source, and Plan Type.



# Task 2: Define the North Star Metric

## North Star Metric

**Paid Conversion Rate**

**Formula:**

> **Paid Conversion Rate = (Number of Users Converted to Paid ÷ Total Users) × 100**

### Why is this the North Star Metric?

* The primary goal of the onboarding campaign is to increase the number of users who become paying customers.
* Paid conversions directly contribute to the company's revenue and long-term business growth.
* Unlike intermediate metrics such as landing page visits or trial starts, paid conversion reflects the complete user journey from signup to becoming a customer.
* It is the most meaningful indicator of whether the new onboarding experience is delivering business value.

### Why are Other Metrics Supporting Metrics?

The following metrics help explain **why** the Paid Conversion Rate increased or decreased but do not directly measure business success.

| Supporting Metric    | Why it is a Supporting Metric                                                        |
| -------------------- | ------------------------------------------------------------------------------------ |
| Visited Landing Page | Measures initial interest but does not indicate user activation or revenue.          |
| Started Trial        | Indicates user activation but not whether users become paying customers.             |
| Completed Onboarding | Shows onboarding effectiveness but does not guarantee conversion.                    |
| Revenue (30 Days)    | Measures financial outcome but can be influenced by pricing, plan mix, or discounts. |
| Engagement Score     | Indicates product usage and user interest but does not always lead to payment.       |
| Days to Convert      | Measures conversion speed rather than the number of paying customers.                |
| Support Tickets      | A guardrail metric that monitors customer experience.                                |
| Refund Requested     | A guardrail metric that monitors customer satisfaction after purchase.               |

### How the North Star Metric Connects to Business Growth

Improving the Paid Conversion Rate benefits the business by:

* Increasing subscription revenue.
* Improving customer acquisition efficiency.
* Generating higher lifetime value (LTV) from acquired users.
* Improving the return on marketing and onboarding investments.
* Supporting sustainable growth by converting more users without necessarily increasing acquisition costs.

### Risks of Optimizing Only This Metric

Focusing only on the Paid Conversion Rate could create unintended consequences, such as:

* Using aggressive tactics that increase conversions but also increase refund requests.
* Encouraging users to subscribe before they fully understand the product, leading to dissatisfaction.
* Increasing customer support tickets due to a confusing onboarding process.
* Prioritizing short-term conversions over long-term engagement and customer retention.
* Ignoring user experience, which could negatively impact brand reputation and customer loyalty.

Therefore, the Paid Conversion Rate should always be evaluated alongside guardrail metrics such as Support Tickets, Refund Requests, User Engagement, and Revenue to ensure the business achieves sustainable growth.


# Task 4: Data Cleaning and Preparation

Before analyzing the experiment results, the dataset was validated to ensure data quality and reliability.

## Data Quality Checks Performed

### 1. Missing Values

**Objective:** Identify missing or blank values in all columns.

**Checks Performed:**

* Verified that all mandatory fields contained valid values.
* Reviewed numerical and categorical columns for null or blank entries.

**Handling:**

* If missing values were found in critical fields (e.g., `experiment_group`, `converted_to_paid`), they were investigated and handled appropriately.
* Missing values in non-critical fields were documented and retained only if they did not impact the analysis.

---

### 2. Experiment Group Counts

**Objective:** Verify that users were correctly assigned to the Control and Treatment groups.

**Checks Performed:**

* Counted the number of users in each experiment group.
* Compared the distribution to ensure the groups were reasonably balanced.

**Handling:**

* No changes were made unless incorrect or invalid group labels were identified.

---

### 3. Duplicate User IDs

**Objective:** Ensure each user appears only once in the experiment.

**Checks Performed:**

* Checked the `user_id` column for duplicate records.

**Handling:**

* Duplicate records, if found, were reviewed.
* Exact duplicates were removed.
* Conflicting duplicate records were investigated before deciding which record to retain.

---

### 4. Invalid Binary Values

**Objective:** Validate binary fields used in the analysis.

**Columns Checked:**

* `visited_landing_page`
* `started_trial`
* `completed_onboarding`
* `converted_to_paid`
* `refund_requested`

**Checks Performed:**

* Verified that each field contained only valid binary values (e.g., Yes/No or 1/0).

**Handling:**

* Invalid or inconsistent values were corrected where possible using business rules.
* Records with unresolvable invalid values were documented and excluded if necessary.

---

### 5. Revenue Outliers

**Objective:** Detect unusually high or low values in `revenue_30d`.

**Checks Performed:**

* Reviewed the revenue distribution using summary statistics.
* Identified potential outliers using the Interquartile Range (IQR) method.

**Handling:**

* Outliers were investigated to determine whether they represented genuine customer behavior or data errors.
* Valid business transactions were retained.
* Data entry errors, if identified, were corrected or removed.

---

### 6. Segment Distribution Across Groups

**Objective:** Ensure the Control and Treatment groups have a similar distribution across key user segments.

**Segments Reviewed:**

* Region
* Device Type
* Traffic Source
* Plan Type

**Checks Performed:**

* Compared the number of users in each segment across both experiment groups.

**Handling:**

* Significant imbalances were documented because they could influence experiment results.
* No records were modified unless data quality issues were identified.

---

## Summary

The dataset was validated for completeness, consistency, uniqueness, and balance before analysis. These quality checks ensure that the experiment results are reliable and that any observed differences between the Control and Treatment groups are more likely to reflect the impact of the onboarding campaign rather than data quality issues.

