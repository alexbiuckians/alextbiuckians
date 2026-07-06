# Alex Biuckians | Data Scientist & Machine Learning Portfolio

I am an M.S. Data Science student at George Washington University specializing in production-grade machine learning systems. I bridge the gap between raw data and deployed intelligence by integrating CI/CD pipelines, containerization, and MLOps best practices with rigorous predictive modeling. My work focuses on building robust, explainable systems that move beyond notebooks into real-world utility.

### 🛠 Featured Projects
I translate complex data into system-level solutions. Here are my current flagship projects:

* **LungGuard**
   * **Problem:** Predicting individual lung cancer risk for clinical decision support.  
   * **Solution:** Benchmarked Logistic Regression, Random Forest, and LightGBM models using 5-fold stratified cross-validation across 29 patient variables. Added SHAP explanations, probability calibration, fairness auditing, and a counterfactual “What-If” engine.  
   * **Outcome:** Deployed an interactive Streamlit dashboard with real-time risk stratification and interpretable model outputs.

* **ClaimsGuard**
   * **Problem:** Identifying high-risk healthcare claims for fraud review.  
   * **Solution:** Built an anomaly-detection system that tiers claims into a prioritized auditor worklist and pairs each flagged claim with SHAP-based explanations.  
   * **Outcome:** Improved top-tier fraud precision from 72% to 80% on a held-out test split after validating a feature-pruned model.

* **Parquet Capital**
   * **Problem:** Assessing NBA player performance trajectories and contract value.  
   * **Solution:** Built an end-to-end machine learning pipeline with quantile-based uncertainty bands, expanding-window time-series validation, and SHAP-based explainability.  
   * **Outcome:** Translated model outputs into contract valuation, salary-efficiency insights, and held-out dollar-impact estimates.

* **UpliftIQ**
   * **Problem:** Maximizing retention contact efficiency by distinguishing "persuadable" customers from observational noise.
   * **Solution:** Benchmarked S-learner, T-learner, and Causal Forest models on confounded data; deployed the winning model via a FastAPI API with Pydantic validation.
   * **Outcome:** Successfully moved beyond naive treated-vs-control reporting to a production-ready CATE (Conditional Average Treatment Effect) estimation engine.

* **HouseEdge**
   * **Problem:** Detecting adversarial threats in casino gaming, specifically identifying both internal rigging of games and external player advantage-play (e.g., card counting) in real-time.
   * **Solution:** Engineered a two-sided integrity system that simulates game outcomes and utilizes Sequential Hypothesis Testing (SPRT, CUSUM) alongside anomaly detection models (Isolation Forest, Gradient Boosting). The system was deployed as a live surveillance console using Dash.
   * **Outcome:** Successfully quantified the "detectability frontier," achieving ~100% detection of card counters within a median of 83 hands at a 0.4% false-positive rate. Furthermore, the project honestly documented its limitations by engineering a "Wong back-counter" technique that bypasses the detection system entirely at a +1% edge.

* **GridCast**
   * **Problem:** High-variance electricity load forecasting requiring precision and reliability.
   * **Solution:** Engineered a robust pipeline using LightGBM with expanding-window time-series validation. Built a containerized FastAPI inference service with MLflow tracking and a full CI/CD pipeline (linting, unit testing, and smoke tests).
   * **Outcome:** Achieved a 72% reduction in MAE (2.67% vs 9.54% MAPE) over a seasonal-naive baseline.


### 💻 Technical Arsenal
- **Languages & Analytics:** Python, SQL, R, SAS, C++, JavaScript
- **ML & Data Science:** pandas, NumPy, SciPy, scikit-learn, LightGBM, XGBoost, PyTorch, SHAP, causalml, econml, Optuna, SMOTE
- **MLOps & Serving:** FastAPI, Pydantic, Docker, MLflow, GitHub Actions (CI), pytest, ruff, Render deployment, REST APIs
- **Visualization & Apps:** Streamlit, Plotly, Dash, Power BI, Tableau, Matplotlib, seaborn, ggplot2, Shiny/Leaflet
- **Modeling & Analytics:** Regression, Classification, Causal Inference / Uplift Modeling, Time-Series Forecasting & CV, Anomaly Detection, Sequential Hypothesis Testing (SPRT/CUSUM), Model Evaluation, Statistical Analysis


### 🎓 Education
**M.S. in Data Science**
George Washington University — Expected May 2027
- **BA in Sport Management, Minor in Data Analytics & Statistics**,
High Point University — December 2024
### 📄 Need the full breakdown?
[Download My Resume](https://drive.google.com/file/d/1SNlEyyIJ_sdBEJNvHw3hyEQTzllKHuFm/view?usp=sharing)

### 🔗 Let's Connect
[LinkedIn](https://www.linkedin.com/in/alex-biuckians/)

### Portfolio Website
Coming soon
