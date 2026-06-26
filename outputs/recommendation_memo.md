
# Recommendation Memo: Onboarding & Activation Campaign A/B Test

## Executive Summary

An A/B test was conducted to evaluate the effectiveness of a new onboarding and activation campaign (Treatment) against the existing onboarding experience (Control). The objective was to determine whether the new onboarding process should be rolled out to all users based on improvements in user conversion while ensuring that customer experience and revenue quality were not negatively affected.

The analysis evaluated the North Star Metric, supporting KPIs, hypothesis test results, guardrail metrics, and segment-level performance before making a business recommendation.

---

# North Star Metric

**Paid Conversion Rate**

**Formula:**

Paid Conversion Rate = (Number of Paid Conversions ÷ Total Users) × 100

This metric was selected because it directly measures the business objective of increasing the number of paying subscribers and has the strongest impact on subscription revenue.

---

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

| Metric                             | Control  | Treatment | 
| ---------------------------------- | -------- | --------- | 
| User Count                         | **690**  | **710**   | 
| Landing Page Visit Rate            | **XX%**  | **XX%**   |
| Trial Start Rate                   | **XX%**  | **XX%**   |
| Onboarding Completion Rate         | **XX%**  | **XX%**   |
| Paid Conversion Rate               | **XX%**  | **XX%**   |
| Average Revenue per User           | **₹XX**  | **₹XX**   |
| Average Revenue per Converted User | **₹XX**  | **₹XX**   |
| Refund Rate                        | **XX%**  | **XX%**   |
| Support Ticket Rate                | **XX%**  | **XX%**   | 
| Average Engagement Score           | **XX.X** | **XX.X**  | 
| Average Days to Convert            | **XX.X** | **XX.X**  | 

Overall, the Treatment group **(performed better / performed similarly / underperformed)** compared with the Control group based on the primary success metric.

---

# Hypothesis Test Interpretation

A **one-tailed Two-Proportion Z-Test** was conducted to compare the Paid Conversion Rate between the Control and Treatment groups.

### Test Results

* Significance Level (α): **0.05**
* Z Statistic: **3.2640**
* P-value: **0.000549**

### Decision

* **If p-value < 0.05:** Reject the Null Hypothesis.
* **If p-value ≥ 0.05:** Fail to Reject the Null Hypothesis.

### Interpretation

**Treatment is significant:**

The p-value is below the significance level of 0.05, indicating that the improvement in Paid Conversion Rate is statistically significant. This provides evidence that the new onboarding experience performs better than the existing onboarding process.

---

# Guardrail Analysis

The experiment also evaluated key guardrail metrics to ensure that any increase in conversion did not negatively impact customer experience.

### Refund Rate

* Control: **XX%**
* Treatment: **XX%**

**Assessment:** *(Improved / Stable / Increased risk)*

### Support Ticket Rate

* Control: **XX%**
* Treatment: **XX%**

**Assessment:** *(Improved / Stable / Increased risk)*

### Average Days to Convert

* Control: **XX.X days**
* Treatment: **XX.X days**

**Assessment:** *(Faster / Similar / Slower conversions)*

### Engagement Score

* Control: **XX.X**
* Treatment: **XX.X**

**Assessment:** *(Improved / Stable / Declined)*

### Revenue Quality

Average Revenue per Converted User was compared to determine whether the Treatment attracted high-value customers.

**Assessment:** *(Improved / Stable / Lower-quality conversions)*

Overall, the guardrail metrics indicate **(low / moderate / high)** business risk.

---

# Segment-Level Insights

Segment analysis was performed across:

* Region
* Device Type
* Traffic Source
* Plan Type

### Key Findings

* Treatment performed best for: **(e.g., Mobile users, Premium plans, Organic traffic)**.
* Treatment underperformed for: **(e.g., Desktop users, Paid Search traffic)**.

These findings suggest whether the campaign is suitable for a full rollout or only for selected user segments.

---

# Final Recommendation

**Recommendation:** **(Choose ONE)**

* ✅ Launch
* ✅ Do Not Launch
* ✅ Launch Only for Selected Segments
* ✅ Continue Testing

### Justification

The recommendation is based on:

* Performance of the North Star Metric.
* Statistical significance of the hypothesis test.
* Guardrail metric evaluation.
* Segment-level performance.

**Example:**

Although the Treatment improved the Paid Conversion Rate, higher refund rates and increased support tickets suggest potential customer experience risks. Therefore, launching the campaign only for high-performing user segments is recommended while further optimizing the onboarding experience for other users.

---

# Risks and Limitations

* The experiment was limited to the observed sample size and testing period.
* Long-term customer retention and lifetime value (LTV) were not evaluated.
* External factors such as seasonality or marketing campaigns may have influenced user behaviour.
* Some user segments may require larger sample sizes to draw reliable conclusions.

---

# Next Steps

1. Continue monitoring the Paid Conversion Rate after implementation.
2. Track long-term customer retention and lifetime value.
3. Monitor guardrail metrics, including refunds and support tickets.
4. Conduct additional experiments for underperforming user segments.
5. Refine the onboarding experience using user feedback and behavioural insights.
6. Re-evaluate performance after collecting additional data if statistical significance is not achieved.

---

# Conclusion

The experiment demonstrates a structured, data-driven approach to evaluating product changes. The final recommendation considers not only improvements in the Paid Conversion Rate but also customer experience, revenue quality, statistical evidence, and segment-level performance to support an informed business decision.
