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
**[Parquet Capital](https://github.com/alexbiuckians/Parquet-Capital)** — Roster valuation engine treating NBA players as financial assets: quantile performance forecasts with coverage-calibrated uncertainty, contract pricing against market comps, and a PuLP cap optimizer. A decision-level backtest on held-out seasons shows Overvalued flags cost ~8.6× more per delivered value point, with robustness checked across a second target and a second model class. 4,860 real player-seasons, 45 tests.
 
**[SignalText](https://github.com/alexbiuckians/SignalText)** — Dual-model sentiment pipeline over 250k Amazon reviews that reports where a fine-tuned transformer and a zero-shot LLM *disagree*, since that's where automated scoring is least trustworthy. The zero-shot model wins 95.6% vs 90.4% — and the weaker model is the more confident one (0.983 vs 0.906), so confidence and correctness point in opposite directions. FAISS semantic search over the corpus on top.
 
**[TransitAccess](https://github.com/alexbiuckians/TransitAccess)** — Multimodal DC transit accessibility built from raw WMATA GTFS into a 23,092-node graph, then a specification ladder showing the headline equity conclusion is dominated by two rarely-stated modeling choices. The same data and code yield a Q4/Q1 job-access ratio anywhere from 1.1 to 24.8 depending on the travel-time budget and whether boarding waits are counted.
 
**[StreamGuard](https://github.com/alexbiuckians/StreamGuard)** — Event-driven streaming pipeline scoring a high-velocity sensor stream in real time for point anomalies and distribution drift, over Redpanda (Kafka API) with River online ML. Precision 0.93 / recall 0.86 with leakage-safe scoring and late-event handling — and it reports that the anomaly detector flags 0 of 1,782 gradual-drift events, a designed blind spot that's exactly why ADWIN runs alongside it.
 
**[HouseEdge](https://github.com/alexbiuckians/HouseEdge)** — Two-sided casino game-integrity system: simulates fair and subtly-rigged games, then detects both rigging and player advantage play under adversarial adaptation using SPRT/CUSUM and anomaly detection. Quantifies a detectability frontier (~100% detection of a card counter in a median 83 hands at a 0.4% false-positive rate) and exposes its own blind spot with a Wong back-counter that evades it entirely at a +1% edge.
 
**[GridCast](https://github.com/alexbiuckians/GridCast)** — Hourly electricity-load forecasting shipped like production software: LightGBM with expanding-window time-series CV and leakage-safe lag features, served by a FastAPI API that engineers features server-side so training and serving share one code path. Cuts MAE 72% over a seasonal-naive baseline (2.67% vs 9.54% MAPE) on 18,169 held-out hours, with MLflow tracking, Docker, and GitHub Actions CI.
 
**[ExperimentLab](https://github.com/alexbiuckians/ExperimentLab)** — End-to-end experimentation case study across three difficulty levels: a clean A/B test, an experiment with variance reduction and segmentation, and a causal-inference problem where randomization was never possible. Power analysis, SRM checks, CUPED-style adjustment, HTE segmentation, then DiD and PSM agreeing within a point on a +8.2pp Medicaid coverage effect — with each phase naming what would break its result.
 
**[MacroQuant](https://github.com/alexbiuckians/MacroQuant)** — Real-time cross-asset streaming pipeline ingesting twelve instruments across five asset classes plus four macro reference series, resampling ticks to OHLCV on the fly with a live correlation engine and GARCH + LSTM forecasts merged into one overlay. Its two-lane ingestion design polls official sources for non-streamable macro series and tags every proxy fallback explicitly, so substitutions are auditable rather than hidden.
 
**[UpliftIQ](https://github.com/alexbiuckians/UpliftIQ)** — Causal uplift-modeling and retention API that estimates the per-customer treatment effect (CATE) of a retention contact and routes budget to persuadables rather than to whoever looks highest-risk. Benchmarks S-learner, T-learner and Causal Forest on badly confounded observational data (propensity AUC ≈ 0.97), deploys the only learner to beat random targeting, and explicitly declines to report the naive treated-vs-control gap as causal.
 
**[EdgarIQ](https://github.com/alexbiuckians/EdgarIQ)** — Retrieval-augmented Q&A over 20 companies' SEC 10-K filings: ~16,000 chunks embedded into ChromaDB, semantic search for the closest passages, and a local Llama 3.2 answering only from retrieved text with an anti-hallucination guardrail that returns the source chunks alongside every claim. Runs entirely on-device with no paid APIs.
 
**[ClaimsGuard](https://github.com/alexbiuckians/ClaimsGuard)** — Explainable healthcare billing fraud-risk prioritization that tiers claims into an auditor worklist and pairs every flag with SHAP attributions. Its central result is a measured experiment, not an assertion: a SHAP audit showed the Isolation Forest leaning on patient-context features rather than fraud signals, and dropping those columns lifted High-tier precision from 71.7% to 80.0%.
 
**[PathForge](https://github.com/alexbiuckians/PathForge)** — Cold-start career recommender that models skills, projects and jobs as a heterogeneous graph and solves link prediction rather than classification, using Node2Vec embeddings over held-out Student→Job edges. Evaluated against a naive skill-overlap baseline across 10 seeds with paired confidence intervals — cold-start hit rate improves by +0.043, while average precision is reported as a null result.
 
**[LungGuard](https://github.com/alexbiuckians/LungGuard)** — Clinical decision-support prototype predicting lung cancer risk from 29 patient variables, pairing each prediction with a SHAP waterfall and a counterfactual "What-If" engine so a clinician sees both why and what a patient can change. Threshold tuned on F2 for screening recall, with calibration and fairness auditing — and metrics openly flagged as a synthetic-data methodology demonstration rather than predictive evidence.

## Technical Arsenal
 
**Languages & Analytics:** Python, SQL, R, SAS, C++, JavaScript

**ML & Data Science:** pandas, NumPy, SciPy, scikit-learn, LightGBM, XGBoost, PyTorch, tidymodels, SHAP, DALEX, causalml, econml, statsmodels, Optuna, SMOTE, LangChain, ChromaDB

**MLOps & Serving:** FastAPI, Pydantic, Docker, MLflow, GitHub Actions (CI), Evidently, pytest, ruff, Render, REST APIs

**Data & Geospatial:** PostgreSQL, SQLite, GeoPandas, sf, NetworkX, Redpanda/Kafka, River, FAISS, GTFS, Census/ACS

**Visualization & Apps:** Streamlit, Shiny, Dash, Plotly, Leaflet, Power BI, Tableau, Matplotlib, seaborn, ggplot2

**Methods:** Quantile Regression, Causal Inference / Uplift Modeling, Spatial Statistics (Moran's I, LISA), Time-Series Forecasting & CV, Anomaly Detection, Sequential Hypothesis Testing (SPRT/CUSUM), A/B Testing, Difference-in-Differences, Operations Research, Retrieval-Augmented Generation
 
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
