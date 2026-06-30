<div align="center">

[![Typing SVG](https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=700&size=24&pause=1000&color=6E40C9&center=true&vCenter=true&width=780&lines=Archana+Suresh+Patil;ML+Platform+%26+LLMOps+Engineer;vLLM+%C2%B7+Kubernetes+%C2%B7+NVIDIA+GPU+%C2%B7+MCP+%C2%B7+AI+Infra;Open+to+Full-Time+%E2%80%94+No+Sponsorship+Needed)](https://git.io/typing-svg)

<br/>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/archana-suresh-patil-792213245)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/ArchanaChetan07)
[![Email](https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:apatil@sandiego.edu)
[![Location](https://img.shields.io/badge/Sunnyvale%2C%20CA-No%20Sponsorship%20Needed-2ea44f?style=for-the-badge&logo=googlemaps&logoColor=white)](#)

</div>

---

## About Me

**ML Platform & LLMOps Engineer** — I build the infrastructure layer that makes LLMs work reliably in production.

- MS Data Science · University of San Diego · GPA 3.9 · Dec 2025
- Built **5 interconnected LLM infrastructure projects** spanning inference observability, Kubernetes deployment, GPU profiling, benchmarking, and conversational AI ops
- **3 MCP servers** published — Python MCP Weather Server · StoryForge Agent · Job Recommendation Engine
- Built **AI Infrastructure Copilot** — LangGraph + Qdrant RAG + Claude, reduces GPU incident investigation from 40min → 3min
- NLP researcher — BERT emotion detection, BART/T5 summarization, topic modeling with CI/CD
- 48 automated tests · CI/CD with Trivy scanning · Helm charts · OpenTelemetry tracing
- Sunnyvale, CA · Open to full-time · No sponsorship needed

**Open to:** ML Platform Engineer · LLMOps Engineer · AI Infrastructure Engineer · MLOps Engineer · Applied AI Engineer · Founding Engineer (AI)

---

## The vLLM Observability Ecosystem

> Five repos. One coherent platform. Built to serve LLMs reliably at scale.

| Repo | What it does | Key tech |
|---|---|---|
| [ai-inference-observability-platform](https://github.com/ArchanaChetan07/ai-inference-observability-platform) | FastAPI proxy — TTFT, TBT, E2E in every response · 48 tests · CI/CD · ≤31ms P99 overhead | `vLLM` `FastAPI` `Prometheus` `Grafana` `OpenTelemetry` `Helm` `K8s` |
| [KubeInfer](https://github.com/ArchanaChetan07/KubeInfer) | Production K8s inference platform · queue-depth HPA · GitOps · 12 alert rules · 1000 req/min | `Kubernetes` `Helm` `NVIDIA GPU` `vLLM` `GitOps` `HPA` `PDB` |
| [KV-Cache-Profiler](https://github.com/ArchanaChetan07/KV-Cache-Profiler-) | Real-time KV cache hit rate · eviction detection · GPU memory pressure | `vLLM` `Prometheus` `DCGM` `Docker` |
| [LLM-Inference-Benchmarking-Dashboard](https://github.com/ArchanaChetan07/LLM-Inference-Benchmarking-Dashboard) | Live TTFT · TPOT · ITL · E2EL charts · NVIDIA DCGM GPU metrics | `Prometheus` `DCGM` `Docker` `vLLM` |
| [AI-Infrastructure-Copilot](https://github.com/ArchanaChetan07/AI-Infrastructure-Copilot) | Conversational GPU diagnosis · Helm config generation · 40min→3min investigation | `LangGraph` `Qdrant` `RAG` `FastAPI` `Slack` `PostgreSQL` |

```
Internet ──► nginx Ingress (TLS) ──► Request Router ──► vLLM Engine × N (NVIDIA GPU)
                                            │                     │
                                    Queue-depth HPA         PagedAttention
                               (vllm:num_requests_waiting)  Continuous batching
                                            │                     │
                                     Prometheus ──► Grafana  Shared PVC
                                     12 alert rules           (model cache)
                                     OpenTelemetry
```

---

## MCP Server Portfolio

> Microsoft invented MCP · Copilot Studio, Claude Desktop, Cursor compatible

| Server | Tools exposed | Transport |
|---|---|---|
| [Python-MCP-Weather-Server](https://github.com/ArchanaChetan07/Python-MCP-Weather-Server) | `check_weather(location)` — structured JSON, validation, logging | stdio |
| [StoryForge-Agent MCP](https://github.com/ArchanaChetan07/StoryForge-Agent) | `research_topic()` · `create_video_script()` — Gemini + Tavily | stdio via FastMCP |
| [Job-Recommendation MCP](https://github.com/ArchanaChetan07/Real-time-Job-recommendation-system---MCP) | `fetchlinkedin()` · `fetchnaukri()` — live job matching pipeline | stdio via FastMCP |

---

## AI Agents & Applications

| Project | Architecture | Stack |
|---|---|---|
| [AI-Infrastructure-Copilot](https://github.com/ArchanaChetan07/AI-Infrastructure-Copilot) | LangGraph agent graph · Qdrant RAG · PostgreSQL · Slack · Auth middleware · Rate limiting | `LangGraph` `Qdrant` `FastAPI` `Claude` |
| [Multi-Agent Purchasing System](https://github.com/ArchanaChetan07/Multi-Agent-AI-Purchasing-System-with-Google-ADK-AMD-Instinct-GPUs) | Multi-agent procurement workflow · AMD Instinct GPUs · Google ADK | `Google ADK` `AMD GPU` `Python` |
| [Real-time Job Recommendation](https://github.com/ArchanaChetan07/Real-time-Job-recommendation-system---MCP) | GPT-4o resume analysis · live job scraping · MCP server · Streamlit | `GPT-4o` `FastMCP` `Streamlit` `Docker` |
| [StoryForge Agent](https://github.com/ArchanaChetan07/StoryForge-Agent) | Autonomous research + script generation · Gemini · Tavily web search | `FastMCP` `Gemini` `Tavily` |
| [ClinInsight Medical AI](https://github.com/ArchanaChetan07/Clinisight-medical-AI-assistant) | Clinical AI assistant · medical NLP · conversational interface | `LangChain` `Python` |

---

## NLP & Machine Learning

| Project | Task | Model | Result |
|---|---|---|---|
| [EmotiCare](https://github.com/ArchanaChetan07/EmotiCare_-AI-Powered-Mental-Health-Assistant) | Emotion detection · crisis support · chatbot | BERT fine-tuned | ⭐ 1 star · crisis_detector + chatbot_engine |
| [TextSummarizer](https://github.com/ArchanaChetan07/TextSummarizer-NLP-Transformer-Hugging-face) | Abstractive summarization | BART / T5 fine-tuning | CI/CD · Docker · src layout |
| [Topic Modeling](https://github.com/ArchanaChetan07/Topic-Modeling) | LSA · NMF · LDA · coherence tuning | Gensim · spaCy · pyLDAvis | CI (3 Python versions) · pre-commit |
| [NLP Political Leaning](https://github.com/ArchanaChetan07/NLP-for-Political-Leaning-Detection) | Political bias detection in text | TF-IDF · Naive Bayes · SVM | Multi-class classification |
| [Sentiment Analysis](https://github.com/ArchanaChetan07/Sentiment-Analysis-on-Text) | Multi-class sentiment pipeline | Transformers · VADER | Full NLP pipeline |
| [Fraud Detection](https://github.com/ArchanaChetan07/Credit-Card-Transactions-Fraud-Detection-Project) | Imbalanced fraud detection (0.17% fraud rate) | XGBoost · CatBoost · SMOTE | 86% recall |
| [Traffic Forecasting](https://github.com/ArchanaChetan07/Metro-Interstate-Traffic-Volume-Forecasting) | Time-series highway volume forecasting | LSTM · TensorFlow | Sequence modeling |

---

## Tech Stack

<div align="center">

**AI Infrastructure & LLMOps**

![vLLM](https://img.shields.io/badge/vLLM-Inference%20Engine-FF6B35?style=flat-square)
![NVIDIA](https://img.shields.io/badge/NVIDIA-GPU%20%7C%20DCGM-76B900?style=flat-square&logo=nvidia&logoColor=white)
![OpenTelemetry](https://img.shields.io/badge/OpenTelemetry-OTLP-000000?style=flat-square&logo=opentelemetry&logoColor=white)
![HuggingFace](https://img.shields.io/badge/HuggingFace-Transformers-FFD21E?style=flat-square&logo=huggingface&logoColor=black)
![LangGraph](https://img.shields.io/badge/LangGraph-Agent%20Orchestration-1C3C3C?style=flat-square)
![LangChain](https://img.shields.io/badge/LangChain-RAG-1C3C3C?style=flat-square)

**Platform & Orchestration**

![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![Helm](https://img.shields.io/badge/Helm-0F1689?style=flat-square&logo=helm&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![ArgoCD](https://img.shields.io/badge/ArgoCD-GitOps-EF7B4D?style=flat-square&logo=argo&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)

**Observability**

![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white)
![Alertmanager](https://img.shields.io/badge/Alertmanager-12%20Rules-E6522C?style=flat-square&logo=prometheus&logoColor=white)

**Agentic AI & MCP**

![MCP](https://img.shields.io/badge/MCP-3%20Servers%20Published-6E40C9?style=flat-square)
![Qdrant](https://img.shields.io/badge/Qdrant-Vector%20DB-DC244C?style=flat-square)
![Claude](https://img.shields.io/badge/Claude-Anthropic-CC785C?style=flat-square)
![GPT-4o](https://img.shields.io/badge/GPT--4o-OpenAI-412991?style=flat-square&logo=openai&logoColor=white)
![Gemini](https://img.shields.io/badge/Gemini-Google-4285F4?style=flat-square&logo=google&logoColor=white)

**ML & NLP**

![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikit-learn&logoColor=white)
![BERT](https://img.shields.io/badge/BERT-Fine--tuning-8B5CF6?style=flat-square)
![BART](https://img.shields.io/badge/BART%2FT5-Summarization-8B5CF6?style=flat-square)

**CI/CD & Security**

![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![Trivy](https://img.shields.io/badge/Trivy-CVE%20Scanning-1904DA?style=flat-square)
![Cosign](https://img.shields.io/badge/Cosign-Keyless%20Signing-0D1B2A?style=flat-square)
![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=flat-square&logo=python&logoColor=white)

</div>

---

## GitHub Stats

<div align="center">

<img height="160" src="https://github-readme-stats.vercel.app/api?username=ArchanaChetan07&show_icons=true&theme=tokyonight&hide_border=true&count_private=true" />
<img height="160" src="https://github-readme-stats.vercel.app/api/top-langs/?username=ArchanaChetan07&layout=compact&theme=tokyonight&hide_border=true" />

</div>

<div align="center">

[![GitHub Streak](https://streak-stats.demolab.com?user=ArchanaChetan07&theme=tokyonight&hide_border=true)](https://git.io/streak-stats)

</div>

---

## What I Build

**ML Platform & LLMOps Engineer** — I close the gap between a working model and one serving production traffic reliably.

Most teams can train a model. Few can serve it at scale. I build the layer in between:

- **GPU-aware Kubernetes scheduling** — right model on right hardware, production-grade Helm charts
- **Inference-specific autoscaling** — HPA on queue depth (`vllm:num_requests_waiting`), not CPU
- **Full-stack observability** — TTFT/TBT/E2E in every response, 12 Alertmanager rules, OpenTelemetry traces
- **Agentic systems** — LangGraph workflows, Qdrant RAG, MCP servers for Copilot Studio and Claude Desktop
- **NLP pipelines** — BERT fine-tuning, BART/T5 summarization, topic modeling with production CI/CD

**Open to full-time roles:** MLOps · ML Platform Engineering · LLMOps · AI Infrastructure · Applied AI · Founding Engineer (AI)

Sunnyvale, CA · No sponsorship needed · Available now
apatil@sandiego.edu

---

<div align="center">

![Profile Views](https://komarev.com/ghpvc/?username=ArchanaChetan07&style=flat-square&color=6E40C9&label=Profile+Views)
[![GitHub followers](https://img.shields.io/github/followers/ArchanaChetan07?style=flat-square&color=6E40C9&label=Followers)](https://github.com/ArchanaChetan07)

<sub>MS Data Science · University of San Diego · GPA 3.9 · Dec 2025 · Built with kubectl, pytest, and too much Prometheus</sub>

</div>
