# Awesome-Data-Transformation-Modeling

## Top Data Transformation & Modeling Ecosystem



**Curated List of SaaS Products & Open-Source GitHub Projects**  

*Focused on SQL-First Modeling, Visual Pipelines & Schema Evolution*  

**Last updated: October 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **Data Transformation & Modeling**. These tools enable analytics engineers and data teams to build, test, and deploy transformation pipelines inside their warehouse—from code-first frameworks that treat SQL models like software to visual canvases that generate governed SQL for analysts.



**Examples** include dbt, Coalesce, Matillion, Fivetran Transform, Databricks Lakehouse, AWS Glue, Talend Data Fabric, Informatica Cloud, Keboola, and Prophecy (the category leaders).



**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, SQL modeling, and open transformation infrastructure—ideal for analytics engineers, data teams, and organizations seeking transparent, vendor-independent data modeling.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



- [Sector Overview & Market Dynamics](#sector-overview--market-dynamics)
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## Sector Overview & Market Dynamics

The global data integration and data transformation software market is valued at approximately **$14B–$20B in 2026** and is projected to expand toward **$35B–$47B+ by the mid-2030s** at an estimated **11%–14% CAGR**, propelled by real-time analytics and enterprise AI/LLM readiness pipelines. The sector is **moderately fragmented yet anchored by a concentrated core**: hyperscalers (AWS, Microsoft, Google) and legacy data management titans (Informatica, Talend/Qlik) dominate high-governance enterprise workloads, while agile cloud-native pure-plays (Databricks, Fivetran, Coalesce, Matillion) fiercely contest modern lakehouse and warehouse-centric modeling.

## SaaS/Hosted Platforms

| Platform | Estimated Scale / Valuation | Starting Pricing | Free Tier / Trial Limits | Key Capabilities & Best For |
|---|---|---|---|---|
| **AWS Glue** | **~$2.0T+** (Amazon market cap; AWS ARR >$105B) | **$0.44 per DPU-hour** (Glue ETL jobs, 1-min minimum); DataBrew: **$0.48 / 30-min session** & **$0.46 / node-hour** | **Forever free**: First **1,000,000 objects stored** and **1,000,000 requests/month** in AWS Glue Data Catalog (compute ETL jobs billed per-second) | Serverless Spark ETL, visual data preparation (DataBrew), and metadata management for AWS-native cloud architectures. |
| **Databricks Lakehouse** | **$134B** (valuation, Series L) | **$0.15 / DBU** (Data Engineering jobs / pipelines) to **$0.22 / DBU** (SQL Warehouses); serverless pay-as-you-go | **14-day free trial** with up to **$400 in usage credits** (full commercial evaluation); also provides a **Community / Free Edition** restricted to non-commercial learning with 1 2X-Small SQL warehouse and daily fair-usage caps | Unified lakehouse platform leveraging Delta Live Tables, Spark SQL, and Unity Catalog governance for data and ML pipelines. |
| **Informatica Cloud** | **~$7.5B** (market cap / ~$1.6B ARR) | **~$90–$100 per IPU/month** via pre-purchased capacity tiers (entry enterprise contracts typically start at **$80,000/year**) | **Forever free tier**: **25 IPUs (Informatica Processing Units) per month** on Cloud Data Integration Free Service; or **30-day full feature trial** | Enterprise data integration and governance platform with extensive pre-built enterprise connectors (SAP, mainframe). |
| **Fivetran Transform** | **$5.6B** (valuation; >$325M ARR) | **~$500 per million MAR** on Standard plan (+ **$5/month floor per connection**) | **Forever free tier**: Up to **500,000 connector MAR/month**, **3,500 activation MAR/month**, and **5,000 monthly model runs** (dbt Core / SQL transforms) | Managed transformation and ELT layer integrated directly into Fivetran's automated pipeline ecosystem. |
| **Talend Data Fabric** | **~$3.1B** (acquired by Qlik / ~$400M+ revenue) | **~$30,000/year** entry-level quote for Qlik Talend Cloud Standard (volume-metered by GB/TB transferred) | **14-day free trial** with unrestricted pipeline access and a **7-day historical sync grace period** (desktop Open Studio was retired in 2024) | Enterprise data integration, cataloging, and stewardship workflows across hybrid and complex multi-cloud environments. |
| **Matillion** | **$1.5B** (valuation; ~$80M ARR) | **~$2.00–$3.50 per credit** on consumption plans; pipelines meter at **3 credits/task-hour for transforms** and **1 credit/task-hour for orchestration** | **14-day free trial** with **500 free usage credits** and unrestricted access to all platform components and connectors | Visual, drag-and-drop cloud-native ELT platform pushing SQL transformations down into Snowflake, Databricks, Redshift, and BigQuery. |
| **Prophecy** | **$268M** (valuation; ~$30M ARR) | **Starter plan at $0**; **Professional at $150/user/month** (includes 50 credits/user/month); **Enterprise Express at $4,000/year** (up to 20 users) | **Forever free Starter plan**: **20 credits/month**, embedded DuckDB execution, and 5 transpiler imports/month | AI-first visual pipeline and SQL canvas (Transform Agent, Document Agent) supporting Spark and legacy Alteryx/Informatica transpilation. |
| **Keboola** | **$128M** (valuation; ~$10M ARR) | **Data Craft at €49/user/month** (includes 600 minutes/month, then €0.125/minute); **Data Teams at €79/user/month** | **Forever free tier**: **120 free compute minutes** in month 1, and **60 free minutes/month** thereafter (additional usage billed at $0.14/min) | All-in-one data operations platform offering SQL/Python transformations, native Snowflake storage, MCP agent server, and EU data residency. |
| **Coalesce** | **~$90M–$100M** (est. valuation, $87M raised; ~$20M ARR) | **Starter plan at $500/month** (includes 2,000 credits/month); Enterprise plans custom | **Forever free tier**: Development environments are **always free for individual developers**; **30-day trial** available for team/production features | Column-aware visual data modeling, quality, and cataloging platform generating governed SQL natively for Snowflake. |



## Open-Source GitHub Projects



- **dbt (data build tool)**  

  **Enables data analysts to transform data in their warehouse** (Apache-2.0 for Core) — **the analytics engineering standard** . **Models are SQL files** with **Jinja templating** for reusable logic . **Tests, documentation, and version control** are first-class—**teams treat data models like software code** . **Huge package ecosystem** (`dbt-utils` and friends cover most common needs) and **largest talent pool** . **Fusion engine** (Rust-based) is faster than the legacy Python engine . **Honest weaknesses**: **Python support runs through the warehouse's own runtime** (library availability depends on Snowflake/Databricks) ; **column-level lineage is not native to dbt Core** (requires a catalog or paid tier) . **No native ingestion or orchestration**—pairs with Fivetran/Airbyte for extraction and Airflow/Dagster for scheduling . **The reference implementation for SQL-first transformation** .



- **SQLMesh**  

  **The strongest technical alternative to dbt** (Apache-2.0) — **virtual data environments** for isolated development without separate schemas . **Native column-level lineage** built in . **SQL-first with templating**—similar coding level to dbt, making it **the easiest "next step" for dbt-trained teams** . **Best for**: teams wanting **dbt-like workflow with better environment isolation and native lineage** .



- **Dataform**  

  **SQL transformation tool for BigQuery** (Apache-2.0) — **the BigQuery-native choice** . **SQL-first with assertions and dependency management** . **Best for**: teams committed to **BigQuery** who want a **Google-native transformation layer** .



- **interlace**  

  **Python/SQL-first data platform combining transformation, orchestration, and durable streaming in one process** (MIT) — **the all-in-one open-source alternative** . **Replaces dbt/SQLMesh for transformation, the orchestrator (no Airflow), and the ingestion layer** . **Models are `.sql` files or Python functions** . **Terraform-style plan/apply** with **breaking/non-breaking change classification** and **column-pruned impact analysis** (downstream models with provably identical output reuse tables) . **Checks gate promotion** (10 built-in types plus custom Python functions) . **Runs on DuckDB + DuckLake by default** . **Requires Python 3.12+** . **Best for**: teams wanting a **single daemon for transformation, orchestration, and streaming** without stitching together dbt + Airflow + ingestion tools .



- **unwind-sql**  

  **SQL orchestration with Jinja templating, semantic layer, and lineage at table, column, and value level** (open-source, alpha) — **the deterministic value-lineage choice** . **SQLGlot AST-backed lineage**—traces `raw_orders.gross_sales = 500.0` and `ref_local_taxes.tax_pct = 0.20` through to the final computed value . **Python models participate in the DAG** like any other node (opaque to lineage, but composable) . **Web UI** for DAG exploration . **Optional LLM investigator** explains traces in plain language . **Runs on DuckDB** . **Best for**: teams needing **deterministic value-level lineage** for debugging and compliance .



- **Reble**  

  **Branch-first SQL transformation with environment isolation** (open-source) — **the "git-style branches for data" choice** . **`reble branch create`** freezes every table as of that moment—**twenty runs over three days compute against the same inputs** so changes are attributable to SQL, not data drift . **`reble diff`** shows row-level changes between branches (`+0 added, -36,121 removed, ~214 changed`) before promoting . **`reble promote`** atomic view swaps . **Parallel engineer workflows** with scope overlap detection—**promote refuses with instructions** if a model reads tables changed by another branch . **Best for**: teams wanting **safe, isolated development with row-level diffs before production** .



### Additional Strong Open-Source Options



- **Dataform** — See above. **The BigQuery-native SQL transformation layer** .

- **Rocky** — SQL transformation with **compile-time type inference, column-level lineage, and 35+ diagnostic codes** (open-source) . **Rocky-unique**: **Time Interval materialization** with per-partition execution, `--lookback` for late-arriving data, `--missing` for gap detection, and `--parallel N` for concurrent partition processing . **Compile-time lineage** accessible via CLI with JSON or Graphviz dot output—no warehouse query needed . **Best for**: teams wanting **compile-time validation and partition-level control** .

- Community **n8n** workflows for transformation pipeline scheduling and data quality alerting.



**Frameworks for building custom systems**: Combine **dbt** for SQL-first modeling with **SQLMesh** for virtual environments and native lineage, **interlace** for all-in-one transformation and orchestration, **Reble** for branch-based isolation with row-level diffs, and **unwind-sql** for deterministic value-level lineage—creating a comprehensive open-source data transformation stack.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- Data transformation platforms handling enterprise data must comply with data protection regulations (GDPR, CCPA, etc.) and implement appropriate access controls.

- **The "code-first vs. visual" distinction drives adoption.** **dbt** expects **SQL + Jinja + YAML + Git** fluency—**the largest ecosystem and talent pool**, but **steepest learning curve** . **Coalesce** blends **SQL knowledge with a visual graph**—**faster onboarding for SQL-capable but less engineering-oriented teams** . **Matillion** is **mostly visual with occasional SQL**—**highest user-friendliness, but version control and code review are less natural** . **Replacing a canvas with a repo is a staffing change dressed as a tooling change**—choose based on **who will build pipelines from now on** .

- **Pricing models vary and can surprise.** **dbt Core is free** (open source); **dbt Cloud** is commercial . **Coalesce** has a **free development tier** but **Starter is $500/month** for production . **Matillion** uses **credits** (3/hour for transformation) with **no published dollar-per-credit rate** . **Prophecy** has a **generous free Starter** (20 credits) and **$150/user/month Professional** . **Keboola** charges **compute minutes** with a **free tier** (60 minutes/month after the first). **Model expected transformation volume before committing** .

- **The Matillion ETL sunset is a migration deadline.** **Legacy Matillion ETL 1.78 LTS is supported until November 2026** . **Migration is unavoidable**—the only question is **where you land** . **If your bill is dominated by long-running transformations**, moving to dbt or Coalesce **drops the per-task-hour meter** . **If your analysts build the pipelines**, staying on a canvas or moving to Coalesce **preserves the staffing model** . **Decide deliberately before October** .

- **dbt's Python limitation is real.** **Python support exists but runs through the warehouse's own Python runtime**—your available libraries and execution model depend on Snowflake or Databricks, not on you . **Column-level lineage is not native to dbt Core**—it requires a catalog or paid tier . **SQLMesh and Coalesce provide native column-level lineage** . **interlace and unwind-sql provide value-level lineage** . **Know what you're trading** .

- **Branch-based development is an emerging differentiator.** **Reble's branch-first model** freezes input tables so **every run during development computes against the same state**—you can prove your SQL changed the output, not the data . **`reble diff`** shows **row-level changes before promoting** . **Scope overlap detection** prevents silent data merges . **This is a fundamentally safer development workflow than shared dev schemas** .

- Self-hosted open-source solutions require proper infrastructure management, package maintenance, and ongoing tuning. **Transformation logic trapped in visual canvases has no export path**—migration requires rewriting intent . **Code-first tools avoid this lock-in** .



---



**Made for analytics engineers, data teams, and organizations building transparent data transformation solutions.**  

Let's make Data Transformation & Modeling more open, data-driven, and governed.
