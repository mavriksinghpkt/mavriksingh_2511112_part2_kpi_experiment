# Business Problem Summary

The company conducted an A/B experiment to evaluate whether a new onboarding and activation campaign performs better than the existing onboarding experience. The objective is to determine whether the treatment should be rolled out to all users by comparing its impact on user conversion and early engagement. The decision should only be made if the Treatment group demonstrates clear improvement while maintaining acceptable guardrail metrics such as user retention, user experience, and support requests. The final recommendation will be based on evidence from the experiment to ensure that the benefits outweigh any potential risks.




# Recommendation Memo

Executive Summary

An A/B experiment was conducted to evaluate the effectiveness of a new onboarding and activation campaign. Users were randomly assigned to either the Control group (existing onboarding experience) or the Treatment group (new onboarding experience). The primary objective of the experiment was to determine whether the new onboarding campaign improved user conversion without negatively affecting key business and customer experience metrics.

The experiment results indicate that the Treatment group outperformed the Control group in terms of Paid Conversion Rate. Statistical hypothesis testing confirmed that the improvement was statistically significant. Additional guardrail metrics were also evaluated, and no major business risks were identified. Based on these findings, the new onboarding campaign is recommended for launch.

---

North Star Metric

The selected North Star Metric for this experiment is the "Paid Conversion Rate".

This metric measures the percentage of users who successfully convert from free users to paying subscribers. It directly reflects the effectiveness of the onboarding process and has the strongest connection to revenue growth and long-term business success.

---

KPI Tree Explanation

The KPI Tree was designed to illustrate how improvements in the Paid Conversion Rate are influenced by multiple business drivers.

The primary KPI drivers include:

* User Acquisition
* User Activation
* User Engagement

Each primary driver is supported by additional sub-drivers such as Landing Page Visit Rate, Trial Start Rate, Onboarding Completion Rate, Engagement Score, and Revenue-related metrics. Guardrail metrics including Refund Rate, Support Ticket Rate, and Days to Convert were also incorporated to ensure that improvements in conversion did not negatively affect customer experience or business quality.

---

Experiment Result Summary

The experiment compared the performance of the Control and Treatment groups across multiple performance indicators.

Key findings include:

* Control Users: 693
* Treatment Users: 715
* Control Paid Conversion Rate: 3.17%
* Treatment Paid Conversion Rate: 6.99%

The Treatment group achieved a noticeably higher Paid Conversion Rate, indicating that the new onboarding experience successfully encouraged more users to become paying customers.

---

Hypothesis Test Interpretation

A one-tailed Two-Proportion Z-Test was conducted to determine whether the observed improvement in Paid Conversion Rate was statistically significant.

Results:

* Test Statistic (Z): 3.252
* P-value: 0.00057
* Significance Level (α): 0.05

Since the calculated p-value is less than the significance level, the Null Hypothesis was rejected. This indicates that the improvement in Paid Conversion Rate is statistically significant and is unlikely to have occurred due to random chance.

---

Guardrail Analysis

Although the Treatment group demonstrated a significant improvement in Paid Conversion Rate, additional guardrail metrics were evaluated before making a rollout recommendation.

The following guardrail metrics were reviewed:

* Refund Rate
* Support Ticket Rate
* Average Days to Convert
* Average Engagement Score

The analysis did not identify any substantial increase in refunds or support requests, nor did it reveal meaningful declines in engagement or conversion speed. These findings suggest that the improvement in conversions was achieved without creating significant business or customer experience risks.

---

Segment-Level Insight

Segment-level analysis was performed using user characteristics such as Region, Device Type, and Traffic Source.

The analysis did not reveal any major decline in performance for any individual segment. The Treatment group maintained consistent performance across the evaluated segments, indicating that the new onboarding campaign benefits a broad range of users rather than a single user category.

---

Final Recommendation

Recommendation: Launch

Based on the experiment results, statistical evidence, and guardrail analysis, the new onboarding campaign should be launched for all users.

This recommendation is supported by the following evidence:

* Paid Conversion Rate increased from 3.17% to 6.99%.
* The hypothesis test produced a statistically significant result (p-value = 0.00057).
* No significant business risks were identified through the evaluated guardrail metrics.
* Segment-level analysis did not reveal any meaningful performance decline for specific user groups.

---

Risks and Limitations

Although the experiment produced positive results, several limitations should be considered before large-scale implementation.

* The experiment represents a single testing period and may not capture long-term user behaviour.
* External factors not included in the dataset may influence conversion outcomes.
* Some business metrics may continue to change after users spend more time with the product.
* Future experiments should continue monitoring customer behaviour after rollout.

---

Next Steps

The following actions are recommended after rollout:

1. Launch the new onboarding campaign for all users.
2. Continue monitoring Paid Conversion Rate and other key performance indicators.
3. Regularly review guardrail metrics such as Refund Rate, Support Ticket Rate, and Engagement Score.
4. Perform follow-up A/B tests to further optimize the onboarding experience.
5. Monitor long-term customer retention and revenue growth after implementation.

---

Conclusion

The experiment demonstrates that the new onboarding campaign delivers a statistically significant improvement in Paid Conversion Rate while maintaining stable guardrail metrics and consistent performance across user segments. Based on the available evidence, launching the Treatment onboarding experience is the most appropriate business decision.
