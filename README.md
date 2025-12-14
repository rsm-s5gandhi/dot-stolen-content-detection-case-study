Detecting Stolen Content on DOT — Product Analytics Case Study

A simulated end-to-end product analytics project inspired by real-world content integrity work at large social platforms.

🔍 Objective
Build a detection system for stolen posts on DOT (fictional social platform), quantify ecosystem harm, evaluate fairness across creator groups, and model policy tradeoffs.

🧩 Components
✔ Data generation & similarity modeling
✔ Stolen-content detector (precision/recall, confusion matrix)
✔ Country-level harm analysis
✔ Creator fairness (FN/FP bias, exposure loss)
✔ Policy simulations (baseline vs Hide vs Downrank)
✔ Temporal drift + CTR fairness analysis (7-day rolling averages)
✔ Three dashboards communicating the full story

📊 Dashboards
Screen captures are inside /tableau/.

1. Data & Modeling
TF-IDF similarity + cosine distance to detect duplicates
Thresholding logic to classify stolen vs original
FN/FP classification to compute creator-level harm
Country-level aggregation for fairness analysis
Notebooks in /notebooks/ include full reproducible code.

2. Key Insights
📌 Detection Performance
Model identifies majority of stolen posts correctly
Still meaningful FN/FP mistakes affecting creator reach
📌 Ecosystem Harm
~33 percent of impressions go to predicted stolen content
Harm distributed across markets (IN, GB, US highest)

📌 Creator Fairness
Casual creators receive disproportionately more false negatives
Influencers heavily impacted by false positives in some markets

📌 Policy Simulation
Policy A (Hide stolen) reduces stolen content most but hurts exposure
Policy B (Downrank 50 percent) delivers best tradeoff
Original creators maintain 80.8 exposure index under Policy B

📌 Temporal Analysis
Stolen-content share increases over time (Jun–Sep)
CTR gap between original and stolen content converges → fairness concern
Country-level stolen rates show strong divergence in Aug–Sep

⚠️ Disclaimer
DOT is a fictional platform created solely for analytical demonstration.
No confidential or proprietary data is used in this project.
