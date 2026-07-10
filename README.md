# Alex Biuckians | Data Scientist & Machine Learning Portfolio
 
I am an M.S. Data Science student at George Washington University (May 2027) focused on production-grade machine learning: rigorous, honestly-benchmarked modeling shipped as deployed, tested services. My work targets the questions most models skip — whose decision an intervention can change, how few observations before you know, and whether a result survives a real baseline — and I hold every project to an honest number rather than a flattering one.
 
**Portfolio site:** https://alexbiuckians.github.io/AlexBiuckiansPortfolioSite/
 
## Featured projects
 
**Parquet Capital** — Front-office valuation engine that prices NBA contracts as financial assets.
- *Approach:* Gradient-boosted quantile forecasts of player performance with uncertainty bands calibrated to ~80% empirical coverage against a real roll-forward; a PuLP optimizer for roster construction under the cap.
- *Outcome:* A decision-level backtest on held-out seasons shows Overvalued flags cost ~8.6× more per delivered value point than Undervalued ones, with the signal confirmed across an independent target (VORP) and an independent model class. Built on 4,860 real player-seasons; 45 tests.


**GridCast** — Hourly electricity-load forecasting, shipped like production software.
- *Approach:* LightGBM with expanding-window time-series CV and leakage-safe features, served by a FastAPI inference API that engineers features server-side to eliminate train/serve skew, with MLflow tracking, Docker, and GitHub Actions CI.
- *Outcome:* 72% reduction in MAE (2.67% vs 9.54% MAPE) over a seasonal-naive baseline on 18,169 held-out hours.


**HouseEdge** — Adversarial game-integrity and advantage-play detection.
- *Approach:* Simulates fair and subtly-rigged games, then detects rigging and advantage play under adversarial adaptation using sequential hypothesis testing (SPRT, CUSUM) and anomaly detection, deployed as a live Dash console.
- *Outcome:* Quantified a detectability frontier — ~100% detection of a card counter in a median 83 hands at a 0.4% false-positive rate — and honestly documented the blind spot by building a Wong back-counter that evades detection at a +1% edge.


**MacroQuant** — Real-time cross-asset market intelligence pipeline.
- *Approach:* A streaming, two-lane ingestion design across five asset classes with on-the-fly OHLCV resampling, a live cross-asset correlation engine, and GARCH + LSTM forecasts merged into one overlay, surfaced in a self-refreshing Dash dashboard that degrades into replay mode when markets are closed.
- *Outcome:* An end-to-end streaming data-engineering system with explicit, auditable proxy fallback for non-streamable macro series, deployable to Render.


**UpliftIQ** — Causal uplift-modeling and retention API.
- *Approach:* Benchmarked S-learner, T-learner, and Causal Forest on confounded observational data (propensity AUC ≈ 0.97); deployed the winning learner via FastAPI with Pydantic validation.
- *Outcome:* A production CATE estimation engine that routes budget to persuadable customers — and explicitly declines to report the naive treated-vs-control gap as a causal effect.
*Additional projects — EdgarIQ (retrieval-augmented Q&A over SEC 10-K filings), ClaimsGuard (explainable healthcare fraud-risk prioritization), and LungGuard (explainable lung-cancer risk prediction) — are on the [portfolio site](https://alexbiuckians.github.io/AlexBiuckiansPortfolioSite/).*
 
## Technical Arsenal
 
**Languages & Analytics:** Python, SQL, R, SAS, C++, JavaScript
**ML & Data Science:** pandas, NumPy, SciPy, scikit-learn, LightGBM, XGBoost, PyTorch, SHAP, causalml, econml, Optuna, SMOTE, LangChain, ChromaDB
**MLOps & Serving:** FastAPI, Pydantic, Docker, MLflow, GitHub Actions (CI), pytest, ruff, Render, REST APIs
**Visualization & Apps:** Streamlit, Plotly, Dash, Power BI, Tableau, Matplotlib, seaborn, ggplot2, Shiny/Leaflet
**Modeling & Analytics:** Regression, Classification, Causal Inference / Uplift Modeling, Time-Series Forecasting & CV, Anomaly Detection, Sequential Hypothesis Testing (SPRT/CUSUM), Retrieval-Augmented Generation, Model Evaluation, Statistical Analysis
 
## 🎓 Education
**M.S. in Data Science**
George Washington University — Expected May 2027
- **BA in Sport Management, Minor in Data Analytics & Statistics**,
High Point University — December 2024
## 📄 Need the full breakdown?
[Download My Resume](https://drive.google.com/file/d/1SNlEyyIJ_sdBEJNvHw3hyEQTzllKHuFm/view?usp=sharing)
## Let's Connect
- **Portfolio:** https://alexbiuckians.github.io/AlexBiuckiansPortfolioSite/
- **LinkedIn:** https://www.linkedin.com/in/alex-biuckians/
