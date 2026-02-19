📊 Experiment Performance Dashboard: A/B Testing Analytics for E-Commerce Optimization

A decision-support Power BI dashboard designed to evaluate A/B test performance by analyzing conversion behavior, uplift impact, and statistical significance to guide product rollout decisions.

<img width="1289" height="717" alt="Experiment Performance Dashboard" src="https://github.com/user-attachments/assets/205c4d9c-6c8c-4a8a-8a63-fc39525dfb45" />


1️⃣ Project Overview

This project analyzes an e-commerce A/B test conducted to evaluate whether a new website variation improves user conversion performance compared to the existing control version.

The dashboard translates raw session and order data into structured business intelligence — enabling leadership teams to answer one fundamental question:

Should we roll out the new variation, or keep the control?

2️⃣ Business Context

Digital product teams continuously experiment with UI changes, landing page redesigns, and pricing strategies. However, experimentation without rigorous analysis can lead to:

False-positive conclusions

Revenue loss from premature rollouts

Missed opportunities due to undervalued improvements

This dashboard was developed to ensure experiment outcomes are evaluated using both performance metrics and statistical validation.

3️⃣ Objective

The core objectives of this analysis were to:

Compare Control vs Variation performance

Measure Conversion Rate (CVR) impact

Quantify percentage uplift

Assess statistical significance (Z-test approach)

Estimate potential business impact

4️⃣ Dataset

Dataset Used: Maven Fuzzy Factory – E-Commerce A/B Testing Dataset

The dataset contains:

Website session data

Order-level transaction data

Test variation identifiers (Control / Variation)

Revenue metrics

The data simulates a real-world experiment where traffic is split between two versions of a website to test performance improvement.

5️⃣ Analytical Approach
Step 1: Core Metrics Development

Key performance indicators were defined:

Sessions

Orders

Conversion Rate (CVR)

Conversion Rate = Orders / Sessions

Step 2: Control Benchmark Creation

To evaluate uplift, a benchmark was required:

Control CVR =
CALCULATE(
    [Conversion Rate],
    website_sessions[Test_Variation] = "Control"
)


This isolates baseline performance.

Step 3: Uplift Calculation
CVR Uplift % =
DIVIDE(
    [Conversion Rate] - [Control CVR],
    [Control CVR]
)


This measures relative improvement.

Interpretation:

Positive value → Variation outperforming Control

Negative value → Variation underperforming

Step 4: Statistical Validation (Z-Test)

Beyond descriptive metrics, inferential statistics were implemented.

Using:

Control Sessions

Control Orders

Variation Sessions

Variation Orders

A two-proportion Z-test was calculated to determine whether observed uplift is statistically significant.

This ensures the result is not due to random variance.

6️⃣ Dashboard Structure
Executive KPI Section

**Link** https://app.powerbi.com/links/Z2xsAFPXET?ctid=56c1d497-700b-49cf-8f8d-3dd6b20d522f&pbi_source=linkShare

Total Sessions

Total Orders

Overall Conversion Rate

Control CVR

Variation CVR

CVR Uplift %

Designed for immediate executive-level insight.

Comparative Performance View

Clustered bar visuals compare:

Traffic allocation

Order volume

This confirms experimental balance.

Conversion Analysis

Side-by-side CVR comparison highlights performance gap between versions.

Statistical Significance Indicator

Z-score output with threshold benchmark:

|Z| > 1.96 → Statistically significant at 95% confidence

|Z| ≤ 1.96 → Not statistically significant

This directly supports go/no-go product decisions.

7️⃣ Key Business Insights (Example Interpretation Framework)

Depending on dashboard results:

Scenario A – Significant Positive Uplift

→ Recommend full rollout of Variation
→ Estimate revenue impact based on traffic scaling

Scenario B – Positive but Not Significant

→ Extend test duration
→ Increase sample size

Scenario C – Negative Uplift

→ Do not roll out
→ Conduct qualitative UX review

8️⃣ Business Impact

This dashboard enables:

1. Risk-Controlled Experimentation

Prevents costly decisions based on misleading percentage differences.

2. Revenue Optimization

Quantifies real business impact of conversion changes.

3. Executive Alignment

Translates technical experiment results into business language.

4. Scalable Testing Framework

Reusable analytical model for future experiments.

9️⃣ Tools & Technologies

Power BI Desktop – Dashboard development

Power Query – Data cleaning & transformation

DAX – Measure creation & statistical calculations

Data Modeling – Relationship management

.pbix file format

🔟 Conclusion

This project demonstrates how structured analytics transforms A/B testing from surface-level comparison into a statistically validated decision framework.

It reflects a core business analytics principle:

Performance improvement must be measurable, significant, and financially justifiable before implementation.

It reflects a core business analytics principle:

Performance improvement must be measurable, significant, and financially justifiable before implementation.
