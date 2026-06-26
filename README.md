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

