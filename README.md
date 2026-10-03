# Hi, I'm Sebastián Velasco Ardila 👋

**Data Engineer** · Lakehouse platforms on Databricks and Microsoft Fabric · Medellín, Colombia

I build production data platforms on the Lakehouse paradigm: ingestion pipelines, medallion architectures and data governance for organizations that need their data to be trustworthy, not just available.

Eight years in data, the last five deep in the Azure and Microsoft ecosystem, with previous roles at **Microsoft Colombia**, **TCS** and **NTT DATA**. Economist by training, so the business question comes first and the pipeline second.

---

### 🔭 What I'm working on

- **Federal data ingestion platform on Databricks** for a U.S. public-data nonprofit.
- **Data quality rules product on Databricks** for a U.S. data-research company, live in production.
- **FHIR R4 health interoperability platform** on Microsoft Fabric for Colombia's Ministry of Health, where I lead the technical side: Bronze → Silver → Gold medallion architecture, entity resolution, knowledge-graph embeddings, RAG-based metadata enrichment and data-quality observability over clinical records.
- **M.Sc. thesis:** a *data contracts* framework with active observability on Databricks Unity Catalog, bringing shift-left governance to Bronze → Silver pipelines (Design Science Research).

**Earlier:** architected an Azure and Microsoft Fabric medallion platform consolidating 67+ source systems.

### 🧱 Databricks in production

**Ingestion platform: raw → Bronze → Silver on Unity Catalog (Azure)**

- Pipelines that land U.S. federal datasets (labor, education, immigration, health, elections, budget) as governed Delta tables, orchestrated with Apache Airflow on Astronomer.
- **Incremental by design:** watermark-based loads and Delta `MERGE` on natural keys, so every run is idempotent and safe to re-run.
- **Metadata-driven:** a dynamic DAG factory configured in YAML plus generic Bronze-to-Silver notebooks driven by dataset-mapping files, instead of one hand-written pipeline per dataset.
- **Legacy migration:** moved legacy scrapers into the framework, including replacing 34 fragmented DAGs with a single parameterized one.
- **Cheap freshness checks:** polling sensors run in Airflow and only start Databricks compute when the source has actually published new data.
- **Refresh validation:** Delta history and time travel for rollback points, plus cross-method validation against an independent source to catch silent failures (a run that reports success while loading wrong data).
- Currently designing the monitoring and observability dashboards for the platform's data quality framework.

**Data quality product: Spark rules engine and Lakeview dashboard**

- A rules pipeline that runs quality checks over a de-identified master dataset and publishes results to a Lakeview dashboard used by product, data science and engineering.
- **Rule families:** hard gates, per-source freshness with red/amber/green bands (sources discovered from `information_schema`, not hardcoded), chain integrity and schema-delta detection.
- **Shipped as code:** Databricks Asset Bundles on Serverless compute, versioned Python wheels, and dev → UAT → prod promotion through GitHub Actions.
- **Tested:** `pytest` suites for every rule, `ruff` linting, and a QA regression DAG backed by a reusable comparison utility.

### 🛠️ Tech stack

**Databricks & Lakehouse**
`Databricks` `Unity Catalog` `Delta Lake` `PySpark` `Spark SQL` `Asset Bundles` `Serverless compute` `Lakeview dashboards` `ai_query()` `Microsoft Fabric`

**Orchestration & Cloud**
`Apache Airflow / Astronomer` `Fabric Pipelines` `Azure Data Factory` `ADLS Gen2` `Azure Key Vault` `Event Hubs` `AWS (EMR, Athena, EC2)` `Docker`

**Languages & tooling**
`Python` `SQL` `Pandas` `DuckDB` `pytest` `uv` `ruff` `GitHub Actions` `Git`

**Analytics, ML & AI**
`Power BI / DAX` `scikit-learn` `XGBoost + SHAP` `Prophet / SARIMA` `PyKEEN` `GraphSAGE` `RAG` `GitHub Copilot`

**Practices**
`Medallion Architecture` `Data Contracts` `Data Quality & Observability` `Metadata-driven pipelines` `Idempotent incremental loads` `FHIR R4` `CI/CD` `Gitflow` `Conventional Commits`

### 🎓 Education

- **M.Sc. Data Science**, Universidad Pontificia Bolivariana *(in progress)*
- **Postgraduate Specialization in Business Intelligence**, Universidad Pontificia Bolivariana
- **B.A. Economics**

### 📜 Certifications

- **GitHub Copilot** (GH-300)
- **Microsoft Certified: Azure Data Engineer Associate** (DP-203)
- **Microsoft Certified: Azure Data Fundamentals** (DP-900)
- **Microsoft Certified: Azure Fundamentals** (AZ-900)

*In preparation:* Databricks Certified Data Engineer (Associate, then Professional) · Claude Certified Developer, Foundations

### 🧑‍🏫 Teaching & mentoring

- Mentor of a 12-month **"Junior Analyst to Data Architect"** program: 52 weeks, 8 phases with approval gates, daily lessons and graded exercises.
- Lead of a 9-week study cohort preparing for the **Claude Certified Developer, Foundations** exam.

### 📌 Selected projects

| Project | What it does | Stack |
|---|---|---|
| [Echovita pipeline](https://github.com/velascocafe23/echovita-pipeline) | End-to-end pipeline: web scraping, multi-target storage, SCD Type 2 consolidation and dashboard, with 24 unit tests and one-command Docker deploy | Scrapy, DuckDB, Airflow, Streamlit, Docker |
| [U.S. payroll forecasting](https://github.com/Svelasco9223/Tallerfinal_Velasco_Sebastian) | Time-series forecasting of U.S. nonfarm payroll (1990–2026); Prophet with a COVID regressor cut MAE by 39% against SARIMA | statsmodels, Prophet |
| [NYC Taxi on Hive and Athena](https://github.com/velascocafe23/U3-LAB-HIVE-SVA) | Big-data querying lab over NYC mobility data | AWS EMR, Hive, Athena, S3 |
| [Heart disease prediction](https://github.com/velascocafe23/heart_ds_project) | Predictive modeling on clinical data, run with Gitflow, Conventional Commits and issue-linked branches *(in progress)* | Python, pandas, scikit-learn |
| [ICFES score prediction](https://github.com/velascocafe23/PrediccionResultadoIcfes) | ML models predicting Colombian standardized test outcomes | Python, scikit-learn |

> Most of my production work lives in private client repositories, so the sections above describe it and the table shows what I can share publicly.

### 🌱 Currently learning

The Databricks architecture track, Unity Catalog governance, data contracts, and graph-based data lineage.

### 📫 Get in touch

- LinkedIn: [linkedin.com/in/sebastian-velasco](https://www.linkedin.com/in/sebastian-velasco/)

---

<sub>💬 Spanish (native) · English (professional working proficiency)</sub>
