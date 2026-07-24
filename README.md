# Alex Biuckians | Data Scientist & Machine Learning Portfolio
 
I am an M.S. Data Science student at George Washington University (May 2027) who builds models on real, messy data and holds every one of them to an honest baseline. My work spans spatial statistics, forecasting under uncertainty, operations research, and the production monitoring that starts after a model ships — and each project reports what it can't prove alongside what it can, rather than a flattering number.
 
**Portfolio site:** https://alexbiuckians.github.io/AlexBiuckiansPortfolioSite/
 
## 🔬 Featured projects
 
**[TurnoutLens](https://github.com/alexbiuckians/TurnoutLens)** — U.S. county voter turnout, explained.
 
- **Approach:** An R pipeline over 21,789 county-cycle observations from real MIT Election Lab returns and U.S. Census data, with PostgreSQL window functions, tidymodels benchmarking, DALEX explainability, and spatial statistics (Moran's I, LISA) on the model's residuals — served through a live Shiny/Leaflet map.
- **Outcome:** Demographics alone explain 61% of out-of-sample variance (trained 2000–2020, tested on an unseen 2024), and the residuals cluster at Moran's I = 0.391 (p = 2.2e-290), with LISA clusters naming the same-day-registration states — the model recovers the effect of election law without ever being told it exists. It deliberately drops a lag feature that improves accuracy 19.5% because it masks the demographics and destroys the finding. [Live app](https://alexbiuckians.shinyapps.io/turnoutlens/)

**[RouteCast](https://github.com/alexbiuckians/RouteCast)** — Last-mile delivery dispatch intelligence. 
- **Approach:** 445,295 real parcel deliveries from Alibaba Cainiao's LaDe dataset, cleaned with a documented audit; three LightGBM quantile models predict P10/P50/P90 delivery time leakage-free by construction, feeding a Hungarian assignment optimizer and a SimPy discrete-event staffing simulation.
- **Outcome:** Calibrated uncertainty (P90 covers 88.9% against a 90% target), and a decision the model can act on — the optimizer's edge grows with dispatch radius, but staffing the peak hotspot at ~10 couriers cuts average order time 37%, so staffing, not assignment, is the larger operational lever. [Live dashboard](https://alexbiuckians.github.io/RouteCast/dashboard/)


**[DriftWatch](https://github.com/alexbiuckians/DriftWatch)** — Production monitoring for a deployed credit-default model.
- **Approach:** Instruments every prediction through FastAPI middleware, detects data drift with KS/PSI statistics, reconciles late-arriving labels to measure performance decay separately, tracks latency at p50/p95/p99, and fires hysteresis-gated alerts with a written runbook and CI.
- **Outcome:** Under concept drift the model's F2 falls 0.640 → 0.565 and recall collapses 0.88 → 0.62 **while data drift reads just 4%** — a monitor watching only drift reports "all clear" while the model silently misses 4 in 10 defaults. Real UCI data, honest held-out AUC ≈ 0.78. [Live app](https://driftmonitor.streamlit.app/)

  
## 📦 Also worth a look
 
[Parquet Capital](https://github.com/alexbiuckians/Parquet-Capital) — NBA contract valuation; Overvalued flags cost 8.6× more per delivered value point on held-out seasons · [SignalText](https://github.com/alexbiuckians/SignalText) — a zero-shot LLM beats a fine-tuned transformer 95.6% vs 90.4%, and the weaker model is the more confident one · [TransitAccess](https://github.com/alexbiuckians/TransitAccess) — the same transit data yields equity ratios from 1.1 to 24.8 depending on assumptions nobody states · [StreamGuard](https://github.com/alexbiuckians/StreamGuard) — event-driven streaming anomaly & drift detection over Kafka · [HouseEdge](https://github.com/alexbiuckians/HouseEdge) — adversarial game-integrity detection with a quantified blind spot · [GridCast](https://github.com/alexbiuckians/GridCast) — hourly load forecasting, 72% MAE cut over baseline · [ExperimentLab](https://github.com/alexbiuckians/ExperimentLab) — A/B testing, CUPED, DiD and PSM with honest assumption-checking · [MacroQuant](https://github.com/alexbiuckians/MacroQuant) · [UpliftIQ](https://github.com/alexbiuckians/UpliftIQ) · [EdgarIQ](https://github.com/alexbiuckians/EdgarIQ) · [ClaimsGuard](https://github.com/alexbiuckians/ClaimsGuard)

## Technical Arsenal
 
**Languages & Analytics:** Python, SQL, R, SAS, C++, JavaScript

**ML & Data Science:** pandas, NumPy, SciPy, scikit-learn, LightGBM, XGBoost, PyTorch, SHAP, causalml, econml, Optuna, SMOTE, LangChain, ChromaDB

**MLOps & Serving:** FastAPI, Pydantic, Docker, MLflow, GitHub Actions (CI), pytest, ruff, Render, REST APIs

**Visualization & Apps:** Streamlit, Plotly, Dash, Power BI, Tableau, Matplotlib, seaborn, ggplot2, Shiny/Leaflet

**Modeling & Analytics:** Regression, Classification, Causal Inference / Uplift Modeling, Time-Series Forecasting & CV, Anomaly Detection, Sequential Hypothesis Testing (SPRT/CUSUM), Retrieval-Augmented Generation, Model Evaluation, Statistical Analysis
 
## 🎓 Education
**M.S. in Data Science**
George Washington University — Expected May 2027
**BA in Sport Management, Minor in Data Analytics & Statistics**,
High Point University — December 2024


## 📄 Need the full breakdown?
[Download My Resume](https://drive.google.com/file/d/1SNlEyyIJ_sdBEJNvHw3hyEQTzllKHuFm/view?usp=sharing)


## Let's Connect
- **Portfolio:** https://alexbiuckians.github.io/AlexBiuckiansPortfolioSite/
- **LinkedIn:** https://www.linkedin.com/in/alex-biuckians/
