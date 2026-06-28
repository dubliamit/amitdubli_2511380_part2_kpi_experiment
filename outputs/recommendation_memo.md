
# Recommendation Memo: Onboarding & Activation Campaign A/B Test

## Executive Summary

An A/B test was conducted to evaluate the effectiveness of a new onboarding and activation campaign (Treatment) against the existing onboarding experience (Control). The objective was to determine whether the new onboarding process should be rolled out to all users based on improvements in user conversion while ensuring that customer experience and revenue quality were not negatively affected.

The analysis evaluated the North Star Metric, supporting KPIs, hypothesis test results, guardrail metrics, and segment-level performance before making a business recommendation.

# North Star Metric

**Paid Conversion Rate**

**Formula:**

Paid Conversion Rate = (Number of Paid Conversions ÷ Total Users) × 100

This metric was selected because it directly measures the business objective of increasing the number of paying subscribers and has the strongest impact on subscription revenue.

# KPI Tree Explanation

The KPI tree identifies the key drivers influencing the Paid Conversion Rate.

### Primary Driver 1: User Acquisition

* Landing Page Visit Rate
* Traffic Source Quality

### Primary Driver 2: User Activation

* Trial Start Rate
* Onboarding Completion Rate

### Primary Driver 3: User Engagement & Monetization

* Engagement Score
* Days to Convert
* Average Revenue per User

### Guardrail Metrics

* Refund Rate
* Support Ticket Rate
* Revenue Quality
* Segment-Level Performance

These guardrail metrics ensure that improvements in conversion do not come at the cost of customer satisfaction or long-term business value.

---

# Experiment Result Summary

| Metric                             | Control    | Treatment | 
| ---------------------------------- | --------   | --------- | 
| User Count                         | **690**    | **710**   | 
| Landing Page Visit Rate            | **63.6%**  | **72.4%** |
| Trial Start Rate                   | **25.1%**  | **29%**   |
| Onboarding Completion Rate         | **15.7%**  | **21.1%** |
| Paid Conversion Rate               | **3.2%**   | **7%**    |
| Average Revenue per User           | **51.97**  | **54.26** |
| Average Revenue per Converted User | **1630.1** | **770.4** |
| Refund Rate                        | **0%**     | **0.4%**  |
| Support Ticket Rate                | **14.8%**  | **24.8%** | 
| Average Engagement Score           | **57.03**  | **62.94** | 
| Average Days to Convert            | **8.86**   | **6.4**   | 

Overall, the Treatment group **performed better** compared with the Control group based on the primary success metric.

These results indicate that the **Treatment group performed significantly better than the Control group** in terms of **Paid Conversion Rate**.

# Hypothesis Test Interpretation

## Test Used

**Two-Sample t-Test Assuming Unequal Variances**

## Hypotheses

**Null Hypothesis (H₀):**

There is no difference in the Paid Conversion Rate between the Control and Treatment groups.

H0​: μControl ​= μTreatment​

**Alternative Hypothesis (H₁):**

The Treatment group has a higher Paid Conversion Rate than the Control group.

H1​: μTreatment ​> μControl​

## Summary of Results

| Metric                           |        Value |
| -------------------------------- | -----------: |
| Control Mean (Conversion Rate)   |    **3.19%** |
| Treatment Mean (Conversion Rate) |    **7.04%** |
| Number of Control Users          |      **690** |
| Number of Treatment Users        |      **710** |
| t-Statistic                      |   **-3.291** |
| One-tailed P-value               | **0.000513** |
| Significance Level (α)           |     **0.05** |

---

## Decision Rule

* If **P-value < 0.05**, reject the Null Hypothesis.
* If **P-value ≥ 0.05**, fail to reject the Null Hypothesis.

Since:

**P-value = 0.000513 < 0.05**

the Null Hypothesis is **rejected**.

## Business Interpretation

The Treatment onboarding campaign achieved a **Paid Conversion Rate of 7.04%**, compared with **3.19%** for the Control group.

The observed difference is **statistically significant**, meaning it is very unlikely to have occurred by random chance.

Therefore, there is strong statistical evidence that the new onboarding campaign increases the likelihood of users converting into paying customers.

## Important Business Consideration

While the Treatment significantly improves conversions, the decision should not rely on the North Star Metric alone.
Guardrail metrics revealed the following:

| Guardrail Metric                   | Observation                      | Business Impact                             |
| ---------------------------------- | -------------------------------- | ------------------------------------------- |
| Refund Rate                        | Increased slightly (0.0% → 0.4%) | Low risk                                    |
| Support Ticket Rate                | Increased (14.8% → 24.8%)        | Higher support workload and customer effort |
| Average Revenue per Converted User | Decreased (1,630 → 770)          | Lower revenue quality                       |
| Engagement Score                   | Improved (57.03 → 62.94)         | Positive                                    |
| Days to Convert                    | Reduced (8.86 → 6.40 days)       | Faster customer activation                  |

Although the Treatment successfully increases conversion and accelerates customer activation, the higher support ticket rate and lower average revenue per converted user suggest that the campaign may attract customers who require more assistance or generate less revenue.

# Final Recommendation

**Recommendation: Launch only for selected segments**

### Justification

* Paid Conversion Rate increased significantly (3.19% → 7.04%).
* The hypothesis test confirms that the improvement is statistically significant (**p = 0.000513**).
* Users convert more quickly and show higher engagement.
* Support Ticket Rate increased substantially.
* Average Revenue per Converted User decreased by more than 50%.

Before a full rollout, the company should investigate why support requests increased and why converted users are generating lower average revenue. A phased rollout or targeting the best-performing user segments would help capture the conversion gains while managing these risks.

# Task 8: Guardrail Metrics Evaluation

## Overview

Although the Treatment group achieved a higher Paid Conversion Rate than the Control group, the decision should not be based solely on this improvement. Guardrail metrics were evaluated to determine whether the increase in conversions came at the expense of customer experience or revenue quality.

| Guardrail Metric                   |   Control | Treatment | Assessment                   |
| ---------------------------------- | --------: | --------: | ---------------------------- |
| Refund Rate                        |      0.0% |      0.4% | Slight increase in refunds   |
| Support Ticket Rate                |     14.8% |     24.8% | Significant increase (Risk)  |
| Average Days to Convert            |      8.86 |      6.40 | Improved (Faster conversion) |
| Average Engagement Score           |     57.03 |     62.94 | Improved engagement          |
| Average Revenue per Converted User |  1,630.10 |    770.41 | Significant decrease (Risk)  |


## 1. Refund Rate

The refund rate increased slightly from **0.0%** in the Control group to **0.4%** in the Treatment group.

Although the increase is relatively small, it indicates that a few additional customers requested refunds after experiencing the new onboarding process. This should be monitored after rollout but does not represent a major concern by itself.

**Risk Level:** Low

## 2. Support Ticket Rate

The percentage of users raising support tickets increased from **14.8%** to **24.8%**.

This is a substantial increase and suggests that users in the Treatment group experienced more confusion or required additional assistance during onboarding. Higher support demand can increase operational costs and reduce customer satisfaction.

**Risk Level:** High

## 3. Average Days to Convert

The average number of days required for users to become paying customers decreased from **8.86 days** to **6.40 days**.

This indicates that the new onboarding experience helped users convert more quickly, allowing the business to realize revenue sooner.

**Risk Level:** None (Positive Outcome)

## 4. Engagement Score

The average engagement score increased from **57.03** to **62.94**.

Higher engagement suggests that users interacted more actively with the product after experiencing the new onboarding campaign. Increased engagement is generally associated with stronger product adoption and improved long-term retention.

**Risk Level:** None (Positive Outcome)

## 5. Revenue Quality

Average Revenue per Converted User decreased significantly from **1,630.10** to **770.41**.

Although the Treatment group generated more paying customers, each converted customer contributed substantially less revenue than those in the Control group. This may indicate that the campaign attracted lower-value customers or encouraged conversion into lower-priced plans.

This is an important business risk because increasing the number of paying customers does not necessarily translate into higher profitability.

**Risk Level:** High

## 6. Overall Guardrail Assessment

The Treatment campaign shows several positive outcomes:

* Higher Paid Conversion Rate (3.2% → 7.0%)
* Higher Landing Page Visit Rate
* Higher Trial Start Rate
* Higher Onboarding Completion Rate
* Higher Engagement Score
* Faster Conversion Time

However, two important guardrail metrics deteriorated:

* Support Ticket Rate increased significantly (14.8% → 24.8%).
* Average Revenue per Converted User decreased substantially (1,630.10 → 770.41).

These findings indicate that while the Treatment improves user conversion and engagement, it may also increase support costs and reduce the average value of each converted customer.

## Conclusion

The Treatment onboarding campaign demonstrates promising improvements in user activation and conversion. However, the increased support ticket rate and lower revenue per converted user introduce meaningful business risks.

Before launching the new onboarding experience to all users, the company should investigate the causes of higher support demand and lower revenue quality. If these issues can be addressed, the Treatment has strong potential for broader rollout. Otherwise, a phased rollout or additional experimentation should be considered.

# Risks and Limitations

* The experiment was limited to the observed sample size and testing period.
* Long-term customer retention and lifetime value (LTV) were not evaluated.
* External factors such as seasonality or marketing campaigns may have influenced user behaviour.
* Some user segments may require larger sample sizes to draw reliable conclusions.

# Next Steps

1. Continue monitoring the Paid Conversion Rate after implementation.
2. Track long-term customer retention and lifetime value.
3. Monitor guardrail metrics, including refunds and support tickets.
4. Conduct additional experiments for underperforming user segments.
5. Refine the onboarding experience using user feedback and behavioural insights.
6. Re-evaluate performance after collecting additional data if statistical significance is not achieved.

# Conclusion

The experiment demonstrates a structured, data-driven approach to evaluating product changes. The final recommendation considers not only improvements in the Paid Conversion Rate but also customer experience, revenue quality, statistical evidence, and segment-level performance to support an informed business decision.
