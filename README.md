# Awesome-Kubernetes-Workflow-Engines

## Top Kubernetes Workflow Engines Ecosystem



**Curated List of SaaS Products & Open-Source GitHub Projects**  

*Focused on Container-Native Orchestration, DAG Scheduling & Batch Processing*  

**Last updated: March 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **Kubernetes Workflow Engines**. These tools orchestrate parallel jobs, complex DAGs, ML pipelines, CI/CD workflows, and data processing tasks natively on Kubernetes, leveraging containers as the fundamental execution unit.



**Examples** include Apache Airflow, Astronomer, Argo Workflows, Prefect Cloud, Dagster Cloud, AWS Step Functions, Temporal Cloud, Kubeflow, Google Cloud Composer, and Azure Data Factory (the category leaders).



**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, GitOps integration, and transparent container-native orchestration — ideal for platform engineers, data teams, and ML practitioners building vendor-neutral workflow infrastructure.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [SaaS/Hosted Platforms](#saas-hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **[Astronomer](https://www.astronomer.io/)**  

  Managed Apache Airflow platform with enterprise-grade security, observability, and CI/CD for data pipelines. Eliminates Airflow operational overhead.



- **[Prefect Cloud](https://www.prefect.io/)**  

  Managed orchestration control plane for Prefect flows with hybrid execution — workflows run in your infrastructure while Prefect handles scheduling, observability, and retries .



- **[Dagster Cloud](https://dagster.io/cloud)**  

  Managed Dagster platform with asset-centric orchestration, software-defined assets, and built-in lineage for data engineering teams .



- **[AWS Step Functions](https://aws.amazon.com/step-functions/)**  

  Serverless state machine orchestration with native AWS service integration; can invoke EKS/Kubernetes jobs for hybrid workflows.



- **[Temporal Cloud](https://temporal.io/cloud)**  

  Managed durable execution platform for stateful workflows with automatic retries, timeouts, and long-running process support.



- **[Google Cloud Composer](https://cloud.google.com/composer)**  

  Managed Apache Airflow service on GCP with native integration to BigQuery, Dataflow, and Cloud Storage.



- **[Azure Data Factory](https://azure.microsoft.com/en-us/products/data-factory)**  

  Cloud ETL and orchestration service with pipeline scheduling, data movement, and transformation activities; can trigger Kubernetes jobs.



## Open-Source GitHub Projects



- **[Argo Workflows](https://github.com/argoproj/argo-workflows)**  

  **The de facto standard for Kubernetes-native workflow orchestration** — CNCF Graduated project with 15k+ stars. Each step runs as a container; supports DAGs, artifacts, retries, and massive parallelism. v4.0 adds artifact driver plugins and dynamic parallelism updates without controller restarts .



- **[Apache Airflow](https://github.com/apache/airflow)**  

  The most widely-adopted workflow orchestrator with Python DAG definitions, 1,000+ operators, rich UI, and massive community. Apache Top-Level Project; battle-tested for batch data pipelines .



- **[Tekton](https://github.com/tektoncd/pipeline)**  

  Kubernetes-native CI/CD framework from the CD Foundation with `Task` and `Pipeline` CRDs. More CI-focused than Argo, with excellent GitHub integration and reusable task catalog .



- **[Kubeflow Pipelines](https://github.com/kubeflow/pipelines)**  

  ML pipeline orchestration using Python DSL that compiles to IR and executes on Kubernetes (Argo-backed in classic deployments). Part of the broader Kubeflow ML platform .



- **[Prefect](https://github.com/PrefectHQ/prefect)**  

  Python-native orchestration with `@flow` and `@task` decorators; supports dynamic DAGs generated at runtime. Hybrid execution model balances developer experience with security .



- **[Dagster](https://github.com/dagster-io/dagster)**  

  Asset-centric orchestration modeling workflows as data assets rather than tasks; excellent lineage tracking and dbt integration .



- **[Cadence](https://github.com/uber/cadence)**  

  **Uber's durable execution engine** for fault-tolerant stateful workflows. Apache 2.0 licensed, Linux Foundation hosted. Runs on SQLite for local dev or Cassandra/MySQL/Postgres for production .



- **[Flyte](https://github.com/flyteorg/flyte)**  

  Kubernetes-native ML orchestration with typed Python SDK, strong reproducibility guarantees, and multi-tenant support. Backed by LF AI & Data .



- **[Kestra](https://github.com/kestra-io/kestra)**  

  Declarative, language-agnostic orchestration with YAML-based flows. Event-driven architecture supports schedules, webhooks, Kafka, and S3 triggers; runs on single Docker or Kubernetes cluster .



### Additional Strong Open-Source Options



- **[Furiko](https://github.com/furiko-io/furiko)** — Enterprise-level cron and adhoc job platform for Kubernetes with concurrency policies, retries, and RBAC .

- **[Kontroler](https://github.com/GreedyKomodoDragon/Kontroler)** — Kubernetes-native DAG orchestrator with both YAML and DSL authoring modes .

- **[FUSE](https://github.com/open-source-cloud/fuse)** — Actor-based workflow engine for AI workflows and agentic orchestration with durable execution .

- **[Kit](https://github.com/kitproj/kit)** — Unified workflow engine for local development combining task execution, service orchestration, and Kubernetes resource management .

- **[Ray + KubeRay](https://github.com/ray-project/ray)** — Distributed compute framework for ML; Ray Workflows is deprecated, but Ray tasks remain excellent for distributed compute inside Argo steps .

- **[Crossplane](https://github.com/crossplane/crossplane)** — Declarative cloud infrastructure provisioning as Kubernetes resources; complements workflow engines for infrastructure automation .

- **[CNCF Landscape](https://landscape.cncf.io/)** — For discovering additional CNCF-hosted orchestration projects.



**Frameworks for building custom systems**: Combine **Argo Workflows** as the orchestration plane with **KubeRay** for distributed compute steps, **Prefect** for Python-native visibility, and **Crossplane** for infrastructure provisioning. For CI/CD, **Tekton** with **Argo CD** enables full GitOps pipelines .



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- Workflow engines manage sensitive infrastructure; implement proper RBAC, secret management, and audit logging.

- Self-hosted solutions require Kubernetes operational expertise and regular security updates.

- Evaluate execution model fit: **run-to-completion** (Argo, Airflow) vs **durable execution** (Cadence, Temporal) vs **continuous reconciliation** (Operators, Crossplane) .



---



**Made for platform engineers, data orchestrators, ML practitioners, and Kubernetes operators.**  

Let's make workflow orchestration more open, portable, and cloud-native.
