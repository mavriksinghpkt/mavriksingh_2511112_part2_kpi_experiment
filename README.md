# Business Context

The company is a subscription-based digital product business that aims to improve user conversion and early engagement through an optimized onboarding experience. To evaluate the effectiveness of a new onboarding and activation campaign, an A/B experiment was conducted where users were randomly assigned to either the existing onboarding experience (Control group) or the new onboarding experience (Treatment group). The objective of the analysis was to determine whether the new onboarding campaign should be launched to all users based on statistical evidence and overall business impact.



# Dataset Description

The dataset contains user-level information collected during the onboarding experiment. It includes experiment group assignment (Control or Treatment), user activity throughout the onboarding journey, conversion status, revenue generated, engagement score, refund requests, support tickets, days to convert, and user segmentation variables such as Region, Device Type, Traffic Source, and Plan Type. This dataset was cleaned and prepared before performing the experiment analysis.



# Task 1: Business Problem Statement

The company has recently introduced a new onboarding and activation campaign with the objective of improving user conversion and encouraging higher early engagement among new users. To evaluate the effectiveness of the new campaign, an A/B experiment was conducted in which users were randomly assigned to either the Control group, which experienced the existing onboarding process, or the Treatment group, which experienced the new onboarding campaign. The purpose of conducting this experiment is to determine whether the new onboarding campaign delivers measurable improvements in user behavior compared to the existing onboarding experience before committing to a full-scale rollout.

The primary business problem is to determine whether the new onboarding experience delivers better business outcomes than the existing onboarding process and should therefore be launched to all users. This decision is significant because it will directly impact company leadership, the product management team, the marketing team, and all future users joining the platform. A successful rollout could improve customer acquisition, user activation, and overall business growth, whereas an ineffective rollout could negatively affect the user experience and business performance.

The main success metric for this experiment is the user conversion rate, as the company aims to increase the percentage of users who successfully complete the onboarding process and become active users. In addition to conversion, early user engagement should also improve, indicating that users are interacting with the platform soon after joining and finding value in the onboarding experience.

While achieving higher conversion is important, the company must also carefully monitor guardrail metrics to ensure that the new onboarding campaign does not create unintended negative consequences. Metrics such as user drop-off rate, customer support requests, user retention, and overall user experience should remain stable or improve. An increase in these negative indicators could suggest that the treatment introduces friction despite improving conversions.

Before making a final recommendation, the company requires strong evidence from the A/B experiment. The Treatment group should demonstrate a meaningful improvement in the primary success metrics while maintaining acceptable performance on all guardrail metrics. Only if the results show that the benefits outweigh any potential risks should the new onboarding campaign be recommended for deployment to all users.




# Task 2: Define the North Star Metric

North Star Metric: User Conversion Rate

The North Star Metric selected for this experiment is the User Conversion Rate. This metric measures the percentage of new users who successfully complete the onboarding process and become active users of the platform. Since the primary objective of the new onboarding and activation campaign is to encourage more users to complete the onboarding journey and begin using the product, the User Conversion Rate is the most appropriate metric to evaluate the success of the experiment.

1) Why is this the main success metric?

The User Conversion Rate is the main success metric because it directly measures whether the new onboarding campaign is achieving its intended business objective. A higher conversion rate indicates that more users are successfully completing the onboarding process and becoming active users, which is the primary goal of the experiment. Unlike other metrics, conversion provides a direct measure of how effective the new onboarding experience is in encouraging users to take the desired action. If the Treatment group shows a significant improvement in conversion compared to the Control group, it provides strong evidence that the new onboarding campaign is more effective.

2) Why are other metrics supporting metrics instead of the North Star?

Other metrics such as Early User Engagement, User Retention, User Drop-off Rate, and Customer Support Requests are important because they provide additional insights into user behaviour and the overall quality of the onboarding experience. However, these metrics do not directly measure whether users successfully complete the onboarding process. Instead, they help explain the reasons behind the conversion results and identify any positive or negative side effects of the new campaign. Therefore, these metrics support decision-making but do not represent the primary objective of the experiment, making them supporting metrics rather than the North Star Metric.

3)How does this metric connect to business growth?

The User Conversion Rate has a direct impact on business growth because an increase in conversions means that more new users become active users of the platform. As the number of active users grows, the company has a greater opportunity to increase customer retention, subscription purchases, and long-term revenue. A successful onboarding experience also improves the likelihood that users will continue using the product, recommend it to others, and contribute to sustainable business growth. Therefore, improving the User Conversion Rate supports both short-term campaign success and the company's long-term business objectives.

4)What could go wrong if this metric is optimized blindly?

Although the User Conversion Rate is the most important success metric, focusing only on increasing this metric can lead to poor business decisions. For example, the company might simplify or pressure users into completing the onboarding process without ensuring that they genuinely understand or enjoy the product. This could result in higher customer complaints, increased user drop-off after onboarding, lower retention, or a poor overall user experience. In the long run, these negative effects could reduce customer satisfaction and harm business performance. Therefore, the User Conversion Rate should always be evaluated together with guardrail metrics to ensure that improvements are both meaningful and sustainable.



# KPI Tree Summary

The KPI Tree was built using **Paid Conversion Rate** as the North Star Metric. The primary KPI drivers include User Acquisition, User Activation, and User Engagement. These drivers are supported by metrics such as Landing Page Visit Rate, Trial Start Rate, Onboarding Completion Rate, Engagement Score, and Revenue Metrics. Guardrail metrics including Refund Rate, Support Ticket Rate, and Average Days to Convert were incorporated to ensure that improvements in conversion did not negatively impact overall business performance or customer experience.



# Experiment Analysis Approach

The dataset was first cleaned and validated by checking for missing values, duplicate user IDs, invalid binary values, revenue outliers, and experiment group balance. Summary metrics were then calculated to compare the Control and Treatment groups. Paid Conversion Rate was selected as the primary metric for evaluation. A one-tailed Two-Proportion Z-Test was performed to determine whether the Treatment group achieved a statistically significant improvement. Finally, guardrail metrics and segment-level performance were reviewed before making the business recommendation.



# Task 3: Data Cleaning and Preparation

Before performing the experiment analysis, the dataset was reviewed to ensure that it was accurate, complete, and suitable for analysis. A systematic data quality assessment was conducted to identify missing values, duplicate records, invalid values, outliers, and the distribution of users across experiment groups. The original dataset structure and formatting were preserved while preparing the working copy (`experiment_analysis.xlsx`).

1. Missing Values

The dataset was examined for missing values across all columns. Missing values were identified in the "device_type", "traffic_source", "engagement_score", and "days_to_convert" columns.

Missing values in "device_type" were replaced using the most frequent category (mode).
Missing values in "traffic_source" were also replaced using the mode to maintain consistency within the categorical data.
Missing values in "engagement_score" were filled using the median value because it is less affected by extreme values than the mean.
Missing values in "days_to_convert" were intentionally left unchanged because this field is only applicable to users who successfully converted. Blank values for non-converted users are valid and do not represent missing or incorrect data.

2. Group Counts

The number of users in both experiment groups was verified to ensure that the A/B experiment contained an appropriate distribution of participants.

Control Group: 693 users
Treatment Group: 715 users

The group sizes were sufficiently balanced for comparative analysis, and no modifications were required.

3. Duplicate User IDs

The dataset was checked for duplicate User IDs to verify that each observation represented a valid user record.

Duplicate User IDs were identified during the inspection. However, these records were not removed because the dataset did not provide sufficient evidence to determine whether they were data entry errors or legitimate repeated user records. Since the assignment required verification rather than automatic deletion, the duplicate records were documented without altering the original dataset.

4. Invalid Binary Values

All binary columns were reviewed to ensure that they contained only valid binary values (0 and 1).

No invalid binary values were found during the validation process. Therefore, no corrections were required.

5. Outliers in Revenue

The Revenue column was examined to identify potential outliers.

Although some users generated substantially higher revenue than others, these observations were considered valid business outcomes rather than data entry errors. Since revenue naturally varies across users in subscription-based businesses, no revenue values were removed or modified.

6. Segment Distribution Across Groups

The distribution of user segments across the Control and Treatment groups was reviewed to identify any major imbalance that could influence the experiment results.

The segment distribution appeared reasonably balanced between both experiment groups, indicating that the experiment was conducted on comparable user populations. As a result, no additional adjustments were required before proceeding with the analysis. 

Summary

The dataset was successfully prepared for analysis after completing all required data quality checks. Necessary missing values were handled appropriately, while valid business information and the original dataset structure were preserved. Duplicate records, binary values, revenue outliers, and segment distributions were reviewed and documented before proceeding with the experiment analysis.



# Hypothesis Test Summary

A one-tailed Two-Proportion Z-Test was performed to compare the Paid Conversion Rate between the Control and Treatment groups. The Treatment group achieved a Paid Conversion Rate of 6.99%, compared with 3.17% for the Control group. The calculated p-value (0.00057) was lower than the significance level of 0.05, resulting in rejection of the Null Hypothesis. This indicates that the improvement in Paid Conversion Rate is statistically significant and unlikely to have occurred by random chance.



# Final Recommendation

Based on the experiment results, statistical evidence, and evaluation of guardrail metrics, the new onboarding campaign is recommended for launch to all users. The Treatment group achieved a significantly higher Paid Conversion Rate while maintaining stable guardrail metrics and consistent performance across evaluated user segments. Therefore, launching the new onboarding experience is expected to improve business performance without introducing significant operational or customer experience risks.



# Assumptions and Limitations

- The experiment data accurately represents user behaviour during the testing period.
- Users were randomly assigned to the Control and Treatment groups.
- The analysis assumes that the recorded metrics are complete and accurate after data cleaning.
- The experiment reflects a limited observation period and may not capture long-term customer behaviour.
- External business factors that may influence user conversion were not included in the dataset.



# Screenshots Included

The repository includes the following screenshots as supporting evidence:

- summary_metrics.png
- hypothesis_test_output.png
- kpi_tree_preview.png



# Guardrail Metrics Considered

Although the Treatment group achieved a significantly higher Paid Conversion Rate than the Control group, the final recommendation should not be based only on conversion improvement. Additional guardrail metrics were evaluated to ensure that the new onboarding campaign did not negatively impact the overall user experience or business performance.

1. Refund Rate

The Refund Rate was evaluated to determine whether the increase in paid conversions resulted in a higher number of dissatisfied customers requesting refunds. No unusual increase in refund requests was observed in the Treatment group.

Risk Assessment: Low Risk

2. Support Ticket Rate

The Support Ticket Rate was reviewed to identify whether the new onboarding experience caused confusion or increased the number of users requiring customer support. The results did not indicate any meaningful increase in support requests.

Risk Assessment: Low Risk
3. Average Days to Convert

The Average Days to Convert was evaluated to determine whether users required more time to become paying customers. The Treatment group did not experience any significant delay in conversion compared to the Control group.

Risk Assessment: Low Risk

4. Average Engagement Score

The Average Engagement Score was reviewed to ensure that users remained actively engaged after onboarding. The Treatment group maintained healthy engagement levels, indicating that the improved conversion rate was supported by continued user activity.

Risk Assessment: Low Risk

Overall Evaluation

The evaluated guardrail metrics did not indicate any significant business risk. Refund requests, support tickets, conversion time, and user engagement remained within acceptable levels while the Treatment group achieved a statistically significant improvement in Paid Conversion Rate. Therefore, no major concerns were identified that would prevent the rollout of the new onboarding experience.
