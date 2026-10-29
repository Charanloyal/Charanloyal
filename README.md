# Charan Kumar Reddy

Data, backend and ML engineering · B.Tech ECE (Data Science) at SRM Institute of Science and Technology, graduating May 2027 · AI/ML intern at General Motors, Bengaluru

[Portfolio](https://personal-portfolio-hub-3z4y.onrender.com/) · [LinkedIn](https://www.linkedin.com/in/b-charan-kumar-reddy/) · [Email](mailto:charankumarreddy2028@gmail.com)

I build the parts of a system that decide whether its data and models can be trusted:

- **Data pipelines** — change data capture into a lakehouse, idempotent writes, dead-letter handling, data contracts and quality gates.
- **Backend services** — FastAPI services with rate limiting, caching, circuit breakers and streaming responses, packaged with Docker and tested in CI.
- **ML and AI engineering** — models evaluated against honest baselines, RAG with verified citations and guardrails, and models exported for low-latency serving.

Each project below says how it was tested, what the numbers were measured on, and what it does not do yet. Projects built on synthetic or fictional data are labelled.

## Selected projects

### [LakeFlow](https://github.com/Charanloyal/lakeflow) — CDC lakehouse

PostgreSQL → Debezium → Kafka → Spark Structured Streaming → Apache Iceberg (MinIO) → Trino, with a FastAPI and Next.js control plane.

Change events arrive at least once and sometimes out of order; LakeFlow applies them with LSN-guarded idempotent `MERGE`s and routes malformed records to a dead-letter queue.

An integration test crashes the job between the Iceberg commit and the Kafka offset commit and checks that the replay writes no duplicate rows. Single-node setup; no throughput benchmarks published yet.

[Code](https://github.com/Charanloyal/lakeflow) · [Recorded demo of a CI run](https://charanloyal.github.io/lakeflow/)

### [Vehicle Telemetry Anomaly Detection](https://github.com/Charanloyal/Real-Time-Vehicle-Telemetry-Anomaly-Detection-Edge-ML-Optimization) — streaming ML · synthetic data

Point and per-vehicle window models (scikit-learn, XGBoost), ONNX export, pandas or PySpark micro-batch streaming with state carried across batches, and a FastAPI service.

Slow sensor drifts stay inside the fleet's normal range, so the window model compares each vehicle with its own history: F1 0.962 on the synthetic test split. ONNX Runtime scores one event in 0.042 ms (p50, laptop CPU). Streaming reads files; the Kafka source is not implemented.

[Code](https://github.com/Charanloyal/Real-Time-Vehicle-Telemetry-Anomaly-Detection-Edge-ML-Optimization) · [Live demo](https://vehicle-telemetry-anomaly-detection.onrender.com/)

### [DriveDocs AI](https://github.com/Charanloyal/drivedocs) — multimodal RAG · fictional manual

LangChain tool-calling agent over MiniLM text and CLIP image embeddings in FAISS, with file-and-page citations that are checked before an answer is returned, plus prompt-injection and PII guardrails.

Passes 39/39 QA and 23/23 security cases on evaluation sets written alongside the fictional corpus (in-sample; indicative only). The public demo uses an offline planner and does not call an LLM.

[Code](https://github.com/Charanloyal/drivedocs) · [Live demo](https://drivedocs-3xr4.onrender.com)

### [TicketLens](https://github.com/Charanloyal/ticketlens) — text classification and serving

Compares TF-IDF + Logistic Regression, a Keras CNN and DistilBERT + LoRA on one held-out set of 3,563 IT tickets. TF-IDF + LR scored the best macro-F1 (0.835 vs 0.779 for DistilBERT + LoRA), so it is the model served by FastAPI, with PII scrubbing and confidence-gated routing of uncertain tickets to human review.

[Code](https://github.com/Charanloyal/ticketlens) · [Live demo](https://ticketlens.onrender.com/)

### [FeatureHub + DataGuard](https://github.com/Charanloyal/featurehub-dataguard) — feature store and data reliability · synthetic data

Data contracts, schema diffing and Great Expectations gates run before features are written to Redis; point-in-time joins build training sets, and a failed gate emits an OpenLineage event and files an incident instead of publishing.

Redis online lookup: 0.77 ms p50 / 1.62 ms p99 (one laptop, loopback, single client).

[Code](https://github.com/Charanloyal/featurehub-dataguard)

### [NeuralGateway](https://github.com/Charanloyal/neural-gateway) — LLM gateway prototype

FastAPI gateway with a Redis Lua token-bucket rate limiter, a response cache, EWMA latency routing, circuit breakers, SSE streaming and Kafka audit events. LLM providers are mocked by default; no load benchmarks yet.

[Code](https://github.com/Charanloyal/neural-gateway)

More projects, including experiments and learning projects, are on the [portfolio](https://personal-portfolio-hub-3z4y.onrender.com/#all-projects). The demos run on free hosting, so the first request can take a minute while the service wakes up.

## Tools I use

- **Languages:** Python, SQL, TypeScript / JavaScript
- **Data:** PostgreSQL, Debezium, Apache Kafka, Spark Structured Streaming / PySpark, Apache Iceberg, Trino, Apache Airflow, Great Expectations, Redis
- **Backend:** FastAPI, gRPC, Celery, Docker Compose, GitHub Actions, Prometheus
- **ML and AI:** scikit-learn, XGBoost, PyTorch, Hugging Face Transformers + PEFT (LoRA), TensorFlow / Keras, ONNX Runtime, SHAP, LangChain, LangGraph, FAISS, Qdrant

## Contact

Open to internships and early-career roles in data engineering, backend engineering and ML / AI engineering.

- Email: [charankumarreddy2028@gmail.com](mailto:charankumarreddy2028@gmail.com)
- LinkedIn: [linkedin.com/in/b-charan-kumar-reddy](https://www.linkedin.com/in/b-charan-kumar-reddy/)
- Portfolio: [personal-portfolio-hub-3z4y.onrender.com](https://personal-portfolio-hub-3z4y.onrender.com/)