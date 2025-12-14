🎯 Detecting Stolen Content on DOT — A Product Analytics Case Study

This project applies data science, policy modeling, and product analytics to analyze and mitigate stolen content on DOT, a fictional social media platform created solely for educational and portfolio purposes.

The goal is to evaluate content detection accuracy, understand ecosystem harm, measure creator-level fairness, and test ranking policy interventions designed to reduce stolen content while preserving a healthy creator ecosystem.

📌 Project Overview

Stolen content harms both creators and the broader platform ecosystem—it reduces original creators’ exposure, amplifies repost accounts, and degrades trust.

This case study simulates a full content integrity workflow by:

Modeling stolen content using similarity-based detection

Evaluating detector quality with a confusion matrix

Quantifying ecosystem-level harm (impressions, exposure loss)

Identifying fairness gaps across creator types and countries

Analyzing temporal trends & model drift over time

Testing policy interventions to improve creator outcomes

All data is synthetic and generated for research and demonstration only.

🔍 Methodology
1. Data Preparation

Data Sources: Synthetic DOT datasets including posts, creators, feed impressions, predictions, and fairness labels.

Preprocessing Steps:

Merged posts with predictions & impressions

Normalized timestamps for temporal analysis

Created stolen/original labels

Built country-level and creator-type aggregations

Feature Engineering:

Content similarity indicators (provided in synthetic dataset)

Creator-level originality scores

Exposure metrics

Time-series features (daily content mix, CTR trends)

2. Modeling & Evaluation

The detection model is simulated using cosine-similarity–based matching, producing predicted_stolen labels for all posts.

Evaluation Metrics:

Confusion Matrix (TP, FP, FN, TN)

Stolen Impression Share

CTR (original vs stolen) & CTR gap

Creator exposure index

Country-level and creator-type misclassification rates

3. Insights & Findings
A. Detection Quality

The detector correctly identifies most original posts but still mislabels some stolen posts as original.

False negatives reduce creator exposure, while false positives increase viewer risk by hiding legitimate content.

B. Ecosystem Harm

~33.6 percent of impressions go to stolen posts in the baseline scenario.

Harm varies modestly by country, with all markets affected.

C. Creator Fairness

Business, casual, and influencer creator groups are affected differently by false positives and false negatives.

Originality score ranking highlights which creators consistently post original content.

D. Temporal Trends

Stolen content share increases over time.

The model exhibits drift, with predicted-stolen diverging from actual stolen in late August.

CTR gap analysis shows minimal engagement advantage for original content by the end of the period.

4. Policy Simulation

Three policies were modeled:

Baseline (no intervention)

Policy A: Hide predicted stolen

Policy B: Downrank predicted stolen by 50 percent

Findings:

Policy A reduces stolen impressions most aggressively but significantly reduces creator exposure.

Policy B offers the best tradeoff between reducing stolen content and preserving creator reach.

Exposure index (baseline = 100) drops to 61.6 under Policy A but remains a healthier 80.8 under Policy B.

🛠️ Tools & Technologies

Python: pandas, numpy, matplotlib, seaborn

DuckDB: fast analytics engine for dataset merging

Tableau: dashboarding and visual storytelling

Jupyter Notebook: reproducible end-to-end workflow

Version Control: GitHub for full transparency

💡 Key Skills Demonstrated

Content Integrity & Policy Analytics

Fairness & Exposure Harm Analysis

Time-Series Modeling & Drift Detection

Data Visualization & Dashboard Design

Tradeoff-Driven Product Thinking

Experimentation & Policy Simulation

🚀 Key Takeaways

Stolen content impacts not only detection accuracy but also creator fairness, exposure, and viewer experience.

Policy interventions must balance platform safety and creator economic incentives.

Time-series monitoring is essential to detect model drift early.

Combining model evaluation + fairness analysis + business tradeoffs results in strong, actionable product recommendations.

📊 Dashboards Preview
Dashboard 1 — Detection Quality & Ecosystem Harm

Confusion matrix, post mix, harm by country, and policy tradeoffs.


Dashboard 2 — Creator Fairness & Exposure Impacts

Misclassification fairness, originality ranking, FN/FP breakdown by country, and exposure harm vs viewer risk.


Dashboard 3 — Temporal Trends, Drift & CTR Fairness

Actual vs predicted stolen trends, CTR gap analysis, and stolen share by country over time.


📝 Disclaimer

DOT is a fictional platform created solely for educational and portfolio purposes.
All data used in this project is synthetic and does not represent any real users, real companies, or internal systems.
