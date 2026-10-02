<div align="center">

# Hi, I'm Charan Loyal 👋
### **Distributed Systems & AI Infrastructure Engineer | SDE / FDE / AI-Infra**

*Specializing in High-Throughput Microservices, Consensus Protocols, LLM Serving Gateways & Cloud Infrastructure*

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/)
[![GitHub Repositories](https://img.shields.io/badge/GitHub-Repositories-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Charanloyal?tab=repositories)
[![Email](https://img.shields.io/badge/Email-Contact_Me-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:charanloyal@gmail.com)

---

</div>

## 🚀 About Me

I am a **Systems Infrastructure & Software Development Engineer (SDE)** passionate about building **distributed consensus engines**, **fault-tolerant microservices**, and **AI/LLM serving infrastructure**. My work focuses on low-latency data pipelines, zero-downtime failover systems, and high-throughput backend architecture targeting GCCs and Tier-1 Product Companies.

- ⚡ **Core Domain Focus**: Distributed Systems, Consensus Algorithms (Raft), Async Gateway Architecture, LLM Infrastructure.
- 🛠️ **Engineering Principles**: Clean Code, ACID Durability, Zero-Mock Systems Testing, Automated CI/CD Pipelines.
- 🎯 **Targeting Roles**: Software Development Engineer (SDE-I / SDE-II), Forward Deployed Engineer (FDE), AI Infrastructure Engineer.

---

## 🛠 Tech Stack & Core Competencies

<div align="center">

### **Languages & Core Systems**
![Python](https://img.shields.io/badge/Python-3.11+-3776AB?style=for-the-badge&logo=python&logoColor=white)
![C++](https://img.shields.io/badge/C++-17/20-00599C?style=for-the-badge&logo=cplusplus&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-SQLite/Postgres-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![Bash](https://img.shields.io/badge/Linux/Bash-4EAA25?style=for-the-badge&logo=gnu-bash&logoColor=white)

### **Distributed Systems & Microservices**
![gRPC](https://img.shields.io/badge/gRPC-Protobuf-244c5a?style=for-the-badge&logo=grpc&logoColor=white)
![Raft Consensus](https://img.shields.io/badge/Raft_Consensus-Algorithm-FF6F00?style=for-the-badge)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![Redis Lua](https://img.shields.io/badge/Redis-Lua_Token_Bucket-DC382D?style=for-the-badge&logo=redis&logoColor=white)
![Apache Kafka](https://img.shields.io/badge/Apache_Kafka-Async_Audit-231F20?style=for-the-badge&logo=apachekafka&logoColor=white)

### **AI Infrastructure & Observability**
![Sentence Transformers](https://img.shields.io/badge/Sentence_Transformers-Cosine_Similarity-FF6F00?style=for-the-badge)
![Circuit Breaker](https://img.shields.io/badge/3--State_Circuit_Breaker-EWMA_Routing-8B5CF6?style=for-the-badge)
![Prometheus](https://img.shields.io/badge/Prometheus-Metrics-E6522C?style=for-the-badge&logo=prometheus&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-Compose-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-CI/CD-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)

</div>

---

## 🌟 Flagship Systems & Engineering Projects

### 1. ⚙️ [RaftKV — Distributed Consistent Key-Value Store](https://github.com/Charanloyal/raftkv)
> *Production-grade, strongly consistent distributed key-value store in Python 3.11 using Raft Consensus over gRPC.*

- **Raft Consensus Protocol**: Strictly compliant Raft state machine (Follower, Candidate, Leader), $lastLogTerm$/$lastLogIndex$ log up-to-date validation, and commit index progression.
- **ACID Write-Ahead Logging (WAL)**: SQLite-backed WAL engine (`wal.sqlite`) storing `currentTerm`, `votedFor`, log entries, and atomic snapshot compaction metadata.
- **Smart Client Driver**: Automatic leader discovery, client sequence deduplication, and exponential backoff retry logic.
- **Chaos Testing Harness**: 5-node isolated Docker bridge cluster test asserting leader failover and election convergence in **<1.0s**.

---

### 2. ⚡ [NeuralGateway — Distributed Multi-Tenant LLM Gateway](https://github.com/Charanloyal/neural-gateway)
> *High-throughput LLM serving broker with Redis Lua token bucket rate limiting, semantic vector caching, and EWMA routing.*

- **Atomic Token Bucket Rate Limiting**: Single-roundtrip Redis Lua script eliminating race conditions across gateway replicas with dynamic `Retry-After` headers.
- **Semantic Vector Caching**: L2-normalized dense vector embeddings (`sentence-transformers/all-MiniLM-L6-v2`) with cosine similarity search returning cached SSE completions in **<2ms at $0.00 LLM cost**.
- **EWMA Latency-Weighted Routing & Circuit Breaker**: Exponentially Weighted Moving Average routing with 3-state circuit breakers (`CLOSED` $\rightarrow$ `OPEN` $\rightarrow$ `HALF_OPEN`) for zero-downtime provider failovers.
- **Production Observability**: Prometheus `/metrics` endpoint, non-blocking Kafka audit producer, and interactive Web Control Plane dashboard live on [Render](https://neural-gateway-core.onrender.com/).

---

## 📈 Quantifiable Engineering Impact & Benchmarks

| Project / Component | Key Metric | Engineering Benchmark | Business / Technical Value |
| :--- | :--- | :--- | :--- |
| **RaftKV Cluster Failover** | Sub-Second Convergence | **< 1.0s Leader Re-election** | Zero data loss during hard node failures |
| **RaftKV Throughput** | QPS Operations | **~1,785 GET ops/sec** | High-throughput distributed read performance |
| **NeuralGateway Cache** | Cache Replay Latency | **< 2.0ms Response Time** | Eliminates 100% of LLM token cost on hit |
| **NeuralGateway Limiter** | Atomic Lua Execution | **Single Roundtrip Redis Script** | Zero race conditions across distributed workers |

---

## 📊 GitHub Analytics

<div align="center">

<img height="180em" src="https://github-readme-stats.vercel.app/api?username=Charanloyal&show_icons=true&theme=dark&bg_color=07090e&title_color=06b6d4&text_color=94a3b8&icon_color=10b981&border_color=1e293b" />
<img height="180em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Charanloyal&layout=compact&theme=dark&bg_color=07090e&title_color=06b6d4&text_color=94a3b8&border_color=1e293b" />

</div>

---

## 📬 Connect With Me

- 💼 **LinkedIn**: [Connect on LinkedIn](https://linkedin.com/in/b-charan-kumar-reddy)
- 💻 **GitHub**: [github.com/Charanloyal](https://github.com/Charanloyal)
- 📧 **Email**: [charan.workmaill@gmail.com](mailto:charan.workmaill@gmail.com)
