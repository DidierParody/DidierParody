<div align="center">

# Didier Parody

**Data Engineer** &nbsp;·&nbsp; Building production-grade systems while finishing my CS degree

*Pipelines de datos · Agentes LLM · Arquitectura cloud multi-cloud — desde la universidad, con mentalidad de producción*

</div>

<br>

## About me

- 🎓 Estudiante de Ingeniería en Sistemas — Universidad de Pamplona, Colombia
- 🏗️ Construyo sistemas de datos reales: ETL incremental, modelado dimensional, pipelines multi-cloud (GCP + AWS)
- 🤖 Interesado en la intersección de data engineering con AI: RAG, agentes LLM, graph analytics con Neo4j
- 🎯 Disponible para roles de Data Engineering / Backend Data — Colombia o remoto

<br>

## Tech Stack

**Data & Databases**

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-0D1B2A?style=flat-square&logo=postgresql&logoColor=white)
![PySpark](https://img.shields.io/badge/PySpark-0D1B2A?style=flat-square&logo=apachespark&logoColor=white)
![Neo4j](https://img.shields.io/badge/Neo4j-0D1B2A?style=flat-square&logo=neo4j&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-0D1B2A?style=flat-square&logo=redis&logoColor=white)
![pgvector](https://img.shields.io/badge/pgvector-0D1B2A?style=flat-square&logo=postgresql&logoColor=white)

**Cloud**

![Google Cloud](https://img.shields.io/badge/Google_Cloud-0D1B2A?style=flat-square&logo=googlecloud&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-0D1B2A?style=flat-square&logo=amazonaws&logoColor=white)

**IaC & DevOps**

![Terraform](https://img.shields.io/badge/Terraform-0D1B2A?style=flat-square&logo=terraform&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-0D1B2A?style=flat-square&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-0D1B2A?style=flat-square&logo=githubactions&logoColor=white)
![Cloud Build](https://img.shields.io/badge/Cloud_Build-0D1B2A?style=flat-square&logo=googlecloud&logoColor=white)

**Backend**

![FastAPI](https://img.shields.io/badge/FastAPI-0D1B2A?style=flat-square&logo=fastapi&logoColor=white)
![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy-0D1B2A?style=flat-square&logo=python&logoColor=white)
![Alembic](https://img.shields.io/badge/Alembic-0D1B2A?style=flat-square&logo=python&logoColor=white)

**AI / LLM**

![LangGraph](https://img.shields.io/badge/LangGraph-0D1B2A?style=flat-square&logo=langchain&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI-0D1B2A?style=flat-square&logo=openai&logoColor=white)
![MCP](https://img.shields.io/badge/MCP-0D1B2A?style=flat-square&logo=anthropic&logoColor=white)

**Languages**

![Python](https://img.shields.io/badge/Python-0D1B2A?style=flat-square&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-0D1B2A?style=flat-square&logo=postgresql&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-0D1B2A?style=flat-square&logo=typescript&logoColor=white)

<br>

## Featured Projects

### 🔗 [deluxe-analyze](https://github.com/DidierParody/deluxe-analyze) — Multi-Cloud Graph Analytics Pipeline

CDC pipeline que fluye desde PostgreSQL (AWS RDS) hasta Neo4j (GCP) para detectar comunidades sociales en datos reales de una plataforma de reservas.

![PySpark](https://img.shields.io/badge/PySpark-0D1B2A?style=flat-square&logo=apachespark&logoColor=white)
![Neo4j](https://img.shields.io/badge/Neo4j-0D1B2A?style=flat-square&logo=neo4j&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-0D1B2A?style=flat-square&logo=terraform&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-0D1B2A?style=flat-square&logo=amazonaws&logoColor=white)
![GCP](https://img.shields.io/badge/GCP-0D1B2A?style=flat-square&logo=googlecloud&logoColor=white)

| Qué hace | Decisión técnica |
|---|---|
| CDC: PostgreSQL → Parquet en S3 vía AWS DMS | Replicación lógica sin impacto en producción |
| Event-driven: S3 → Lambda → Pub/Sub → Dataproc Serverless | Desacopla la ingesta del procesamiento batch |
| Louvain + degree centrality con Neo4j GDS | Detección de comunidades a partir de co-asistencia a eventos |
| At-least-once semantics con watermark tracking en GCS | Garantiza idempotencia en reprocessing |
| Infraestructura completa en Terraform + Workload Identity Federation | Multi-cloud sin credenciales hardcodeadas |

---

### 🤖 [deluxe-v2](https://github.com/DidierParody/deluxe-v2) — Agentic Nightclub Booking System

Sistema de reservas conversacional con agentes LLM especializados, doble bot de Telegram (cliente + admin), deployed en AWS ECS.

![LangGraph](https://img.shields.io/badge/LangGraph-0D1B2A?style=flat-square&logo=langchain&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-0D1B2A?style=flat-square&logo=fastapi&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-0D1B2A?style=flat-square&logo=redis&logoColor=white)
![AWS ECS](https://img.shields.io/badge/AWS_ECS-0D1B2A?style=flat-square&logo=amazonaws&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-0D1B2A?style=flat-square&logo=docker&logoColor=white)

| Qué hace | Decisión técnica |
|---|---|
| 5 agentes especializados con LangGraph StateGraph | Separación de responsabilidades por dominio (reservas, pagos, tickets, admin) |
| Multi-model resilience: Gemini 2.5 Flash → Llama 3.3 70B | Fallback automático sin downtime ni cambio de interfaz |
| Idempotency store en Redis | Previene reservas duplicadas en condiciones de rate-limit |
| SQL `FOR UPDATE` en asignación de mesas | Prevención de race conditions bajo concurrencia real |
| Webhooks Telegram (no polling) + doble bot | Baja latencia y separación de flujos cliente/administrador |

---

### 📊 [dwh-spotify-wrapped](https://github.com/DidierParody/dwh-spotify-wrapped) — Spotify Data Warehouse on GCP

Sistema full-stack en producción sobre GCP — ETL incremental de la Spotify API hacia un DWH dimensional en Cloud SQL, con enriquecimiento vía Last.fm y CI/CD automatizado. Proyecto en equipo; mi rol: **backend, modelado dimensional, pipeline ETL y análisis (EDA)**.

![FastAPI](https://img.shields.io/badge/FastAPI-0D1B2A?style=flat-square&logo=fastapi&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL_17-0D1B2A?style=flat-square&logo=postgresql&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-0D1B2A?style=flat-square&logo=terraform&logoColor=white)
![GCP](https://img.shields.io/badge/GCP-0D1B2A?style=flat-square&logo=googlecloud&logoColor=white)

| Qué hace | Decisión técnica |
|---|---|
| Galaxy schema (facts + dims + snowflake element) | Permite drill-through artista/track sin full denormalization |
| Cursor-based incremental load + UNIQUE `(user_id, played_at)` | ETL idempotente: cero duplicados en re-ejecuciones |
| OAuth2 PKCE flow implementado desde cero | No expone client secret al frontend — estándar de seguridad real |
| Cloud SQL en VPC + Secret Manager + IAM least-privilege | Zero credentials en código; backend → DB por red privada via VPC Connector |
| Cloud Build v2: build → push → deploy → migrate automático | Migrations de Alembic aplicadas como Cloud Run Job post-deploy |
| Fallback a Last.fm tras la deprecación de campos de Spotify (nov 2024) | Adaptación a un obstáculo externo sin tocar el modelo dimensional |
| Scheduler nocturno multi-usuario con OIDC (`/v1/etl/run-batch`) | ETL programado y autenticado server-to-server, sin tokens en cron |

<br>

## Currently Learning

- **Streaming**: Kafka + Apache Flink — siguiente paso natural después de trabajar con CDC y Pub/Sub
- **dbt**: Transformaciones declarativas para pipelines más mantenibles y testeables
- **Contacto / Colaboraciones**: torresparodisdidierjose@gmail.com

<br>

---

<div align="center">
  <sub>Construido con decisiones técnicas deliberadas, no con tutoriales.</sub>
</div>
