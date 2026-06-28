# Hypothesis Testing Notes

## Business Context

The company introduced a new onboarding and activation campaign (Treatment) to improve the conversion of new users into paying customers. The objective of this experiment is to determine whether the new onboarding experience should replace the existing onboarding process (Control).

The business decision depends on whether the Treatment group demonstrates a statistically significant improvement in the primary success metric without negatively affecting key guardrail metrics.

# Metric Being Tested

**Primary Metric:** Paid Conversion Rate

**Definition:**

Paid Conversion Rate = (Number of users converted to paid ÷ Total users) × 100

This metric is selected as the **North Star Metric** because it directly measures the company's primary business objective—converting new users into paying subscribers.

# Hypotheses

## Null Hypothesis (H₀)

The new onboarding campaign does **not** improve the Paid Conversion Rate.
H0​: μControl​=μTreatment​

## Alternative Hypothesis (H₁)

The new onboarding campaign **improves** the Paid Conversion Rate.
H1​: μTreatment​ > μControl​

# Type of Test

**A Two-Sample t-Test Assuming Unequal Variances**

### Reason

A Two-Sample t-Test Assuming Unequal Variances was performed in Microsoft Excel to compare the Control and Treatment groups. Since the primary metric is binary (converted/not converted),the t-test indicates a statistically significant improvement in the Treatment group's conversion rate.

# Significance Level

**α = 0.05 (5%)**

This means the company accepts a 5% probability of incorrectly concluding that the Treatment is better when no real improvement exists (Type I Error).

# Why This Metric Was Chosen

Paid Conversion Rate is the most appropriate metric because:

* It directly reflects the success of the onboarding campaign.
* It has a direct impact on subscription revenue.
* It aligns with the company's business objective of increasing paying customers.
* It represents the complete user journey from signup to becoming a paying subscriber.

Supporting metrics such as Trial Start Rate, Onboarding Completion Rate, and Engagement Score help explain user behavior but do not directly measure business success.

# Interpretation Logic

After performing a statistical hypothesis test 

* **If p-value < 0.05**

  * Reject the Null Hypothesis.
  * Conclude that the Treatment significantly improves the Paid Conversion Rate.
  * Proceed to evaluate guardrail metrics before recommending a rollout.

* **If p-value ≥ 0.05**

  * Fail to reject the Null Hypothesis.
  * Conclude that there is insufficient evidence that the Treatment improves conversions.
  * Recommend continuing the experiment or retaining the existing onboarding experience.

# Connection to the Business Decision

The hypothesis test provides statistical evidence to support one of the following business decisions:

* **Launch:** Treatment significantly improves Paid Conversion Rate while guardrail metrics remain stable or improve.
* **Launch for Selected Segments:** Treatment performs significantly better only for specific user segments (e.g., region, device type, or traffic source).
* **Continue Testing:** Improvement is observed but is not statistically significant or the sample size is insufficient.
* **Reject:** Treatment does not improve Paid Conversion Rate or negatively impacts guardrail metrics such as refund rate, support tickets, or revenue quality.

Therefore, the final recommendation will be based on both the statistical significance of the Paid Conversion Rate and the performance of key guardrail metrics to ensure sustainable business growth.

