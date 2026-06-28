# Task 6: Hypothesis Test Notes

Objective

The objective of this hypothesis test is to determine whether the new onboarding and activation campaign (Treatment group) produces a statistically significant improvement in user conversion compared to the existing onboarding experience (Control group). The result of this test will help the company decide whether the new onboarding campaign should be rolled out to all users.

---

Metric Being Tested

Primary Metric: "User Conversion Rate"

The User Conversion Rate measures the percentage of users who successfully convert to a paid subscription after experiencing the onboarding process. Since the primary business objective of the experiment is to improve conversions, this metric serves as the most appropriate measure of success.

---

Null Hypothesis (H₀):

H₀: p(Treatment) = p(Control)

There is no statistically significant difference in the User Conversion Rate between the Treatment group and the Control group.

This means that any observed difference in conversion rates is assumed to have occurred due to random variation rather than the new onboarding campaign.

---

Alternative Hypothesis (H₁):

There is a statistically significant increase in the User Conversion Rate for the Treatment group compared with the Control group.

H₁: p(Treatment) > p(Control)

The User Conversion Rate of the Treatment group is significantly higher than that of the Control group.

This hypothesis supports the business expectation that the new onboarding experience should improve user conversion.

---

Type of Hypothesis Test

A one-tailed hypothesis test will be used.

The purpose of this experiment is not simply to determine whether the Treatment group is different from the Control group, but specifically to determine whether the new onboarding campaign performs better than the existing onboarding experience. Therefore, a one-tailed test is appropriate because the expected direction of improvement is already defined.

---

Significance Level

The significance level (α) is set at 0.05 (5%).

This means that a 5% probability of making a Type I error is considered acceptable. If the calculated p-value is less than 0.05, the null hypothesis will be rejected, indicating that the observed improvement is statistically significant.

---

Reason for Choosing the Metric

The User Conversion Rate was selected because it directly measures the primary objective of the onboarding campaign. An increase in this metric indicates that more users successfully complete the onboarding journey and become paying customers. Compared with other metrics such as engagement score or support tickets, conversion rate has the strongest connection to business performance, customer acquisition, and revenue growth.

---

Interpretation Logic

The final business decision will be based on both statistical significance and practical business impact.

* If the p-value < 0.05 and the Treatment group shows a higher User Conversion Rate than the Control group, the null hypothesis will be rejected. This provides evidence that the new onboarding campaign improves conversions and should be considered for rollout, provided that guardrail metrics remain within acceptable limits.

* If the p-value ≥ 0.05, there is insufficient statistical evidence to conclude that the Treatment group performs better than the Control group. In this case, the company should continue using the existing onboarding process or conduct additional experimentation before making a rollout decision.

---

# Connection to the Business Decision

The hypothesis test directly supports the company's business decision regarding the new onboarding campaign. Rather than relying on observed differences alone, statistical testing helps determine whether the improvement in User Conversion Rate is likely due to the new onboarding experience or simply the result of random variation. This ensures that the rollout decision is supported by reliable evidence, minimizes business risk, and increases confidence in the final recommendation.




# Task 7: Hypothesis Test Results

Summary of Test Inputs

Primary Metric Tested:  "Paid Conversion Rate"

Control Group:
- Total Users: 693
- Converted Users: 22
- Conversion Rate: 3.17%

Treatment Group:
- Total Users: 715
- Converted Users: 50
- Conversion Rate: 6.99%

Statistical Test

Test Used: One-tailed Two-Proportion Z-Test

Significance Level (α): 0.05

Test Statistic (Z): 3.252

P-value: 0.00057

Decision Rule

If the p-value is less than 0.05, reject the Null Hypothesis.

If the p-value is greater than or equal to 0.05, fail to reject the Null Hypothesis.

Since the calculated p-value (0.00057) is less than the significance level (0.05), the Null Hypothesis is rejected.

Business Interpretation

The statistical test shows that the Treatment group achieved a significantly higher Paid Conversion Rate than the Control group. The improvement is statistically significant and is unlikely to have occurred due to random chance. This indicates that the new onboarding campaign successfully increased user conversions.

Based on the hypothesis test, the Treatment should be considered for rollout, provided that the guardrail metrics continue to remain within acceptable limits.
