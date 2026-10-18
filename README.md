# Awesome-Data-Transformation-Modeling

## Top Data Transformation & Modeling Ecosystem



**Curated List of SaaS Products & Open-Source GitHub Projects**  

*Focused on SQL-First Modeling, Visual Pipelines & Schema Evolution*  

**Last updated: October 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **Data Transformation & Modeling**. These tools enable analytics engineers and data teams to build, test, and deploy transformation pipelines inside their warehouse—from code-first frameworks that treat SQL models like software to visual canvases that generate governed SQL for analysts.



**Examples** include dbt, Coalesce, Matillion, Fivetran Transform, Databricks Lakehouse, AWS Glue, Talend Data Fabric, Informatica Cloud, Keboola, and Prophecy (the category leaders).



**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, SQL modeling, and open transformation infrastructure—ideal for analytics engineers, data teams, and organizations seeking transparent, vendor-independent data modeling.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [SaaS/Hosted Platforms](#saas-hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **Coalesce**  

  **Governed data transformation, catalog, and quality platform built for Snowflake** . **Visual, column-aware interface** generates production-grade SQL—positioned between dbt's code-first approach and Matillion's fully visual paradigm . **Column-level lineage and governance** built in, with reusable templates that enforce consistent patterns across teams . **Pricing**: **Free tier available** (development always free); **Starter at $500/month** includes 2,000 credits; Enterprise and Business Critical are custom . **Best for**: teams committed to Snowflake who want **dbt-like control with more visual tooling** and built-in governance .



- **Matillion**  

  **Visual, drag-and-drop cloud-native ETL/ELT suite** covering both ingestion and transformation . **Credit-based consumption model** across Developer, Teams, and Scale editions—**task hours meter at 3 credits/hour for transformation and 1 for orchestration** . **No published dollar-per-credit figure**; public numeric starting price is not shown . **Legacy Matillion ETL reaches end-of-support** (1.78 LTS supported until November 2026) . **Best for**: teams wanting **one commercial vendor for ingestion and transformation with a GUI-first experience**—but expect **migration pressure** as legacy ETL sunsets and **version control/code review are less natural** than code-first tools .



- **Fivetran Transform**  

  **Transformation layer within the Fivetran platform** . **Note**: Fivetran's pricing is **Monthly Active Rows (MAR)** for replication, with **5,000 monthly model runs** included on the free plan for transformations . **Best for**: teams already using Fivetran for ingestion who want **transformations managed in the same platform**.



- **Databricks Lakehouse**  

  **Lakehouse platform with built-in transformation capabilities** via **Delta Live Tables** and **Spark SQL** . **Unity Catalog** governs data and models across the lakehouse . **Best for**: teams already running Spark workloads on Databricks who want **transformations co-located with their data and ML pipelines**.



- **AWS Glue**  

  **Serverless ETL service with DataBrew for visual preparation** . **Pricing**: **$0.44 per DPU-hour** for Glue jobs; **DataBrew at $0.48 per 30-minute interactive session** and **$0.46 per node-hour** for cleaning jobs . **Best for**: AWS-native teams needing **serverless Spark ETL** without managing infrastructure.



- **Talend Data Fabric**  

  **Enterprise data integration and transformation platform** . **Note**: **Qlik Talend Cloud** is the current offering for teams needing **data catalogue and stewardship workflows from the same vendor as the pipelines** . **Best for**: large enterprises with **complex legacy integration** and **governance requirements** .



- **Informatica Cloud**  

  **Enterprise data integration and management platform** with **IPU (Informatica Processing Unit)** consumption model . **Premium connectors** (SAP, Salesforce, mainframe) add **$25,000–$100,000 annually** . **PowerCenter five-year TCO** reportedly ranges **$3.6M to $15M+** for mid-to-large deployments . **Best for**: large enterprises with **complex legacy integration** and **deep regulatory compliance** needs.



- **Keboola**  

  **Unified data platform with ETL/ELT, SQL/Python transformations, and built-in Snowflake storage** . **Pricing**: **Free plan** with **120 free minutes first month, 60 minutes/month after**, **$0.14 per additional minute** . **Data Craft at €49/user/month** (600 minutes then $0.125/minute); **Data Teams at €79/user/month** with 70 Time Credits . **Enterprise** for multi-cloud, private deployments, and compliance . **MCP Server** exposes the platform as callable tools for AI agents . **SOC 2 Type II, GDPR, and HIPAA** available . **Best for**: teams wanting an **all-in-one platform** with transparent compute-minute pricing and **strong European data residency** options .



- **Prophecy**  

  **AI-first data transformation platform with visual pipeline editor and SQL editor** . **Pricing**: **Starter free** (20 credits/month, embedded DuckDB) . **Professional at $150/user/month** (50 credits/user, processing in Databricks/Snowflake/BigQuery) . **Enterprise Express at $4,000** (up to 20 users, billed annually, dedicated SaaS environment, SSO, SCIM, private LLM) . **Enterprise custom** for 20+ users . **Transpiler** imports Alteryx and Informatica workflows (5 imports/month on Starter; 100 on Enterprise Express) . **ISO 27001, SOC 2 Type 2, SOC 1 Type 2, GDPR, CCPA compliant** . **Best for**: teams wanting **AI-assisted pipeline generation** (Transform Agent, Document Agent) with visual review and **legacy Alteryx/Informatica migration** support .



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
