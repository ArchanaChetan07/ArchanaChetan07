# Hi, I'm Archana 👋

**AI/ML Infrastructure Engineer** building LLM inference systems, agentic pipelines, and the observability layer underneath them.

I spend most of my time in three places: making inference faster (vLLM, CUDA, KV-cache), making agents reliable (multi-agent orchestration, MCP, evals), and making both of those measurable (Prometheus, OpenTelemetry, causal evaluation). Currently applying that background to semiconductor design and verification automation at SwanTech AI, after an M.S. in Applied Data Science.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-archanasureshpatil-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://linkedin.com/in/archanasureshpatil)
[![Email](https://img.shields.io/badge/Email-apatil%40sandiego.edu-D14836?style=flat&logo=gmail&logoColor=white)](mailto:apatil@sandiego.edu)

---

### What I build

**Inference infrastructure** — custom CUDA kernels, autoscaling, and observability for LLM serving at production scale.
- [`PagedKV-Fusion`](https://github.com/ArchanaChetan07/PagedKV-Fusion-Custom-CUDA-Kernels-for-KV-Cache-Eviction-Quantized-Paged-Attention) — custom CUDA kernels for KV-cache eviction and INT8 paged attention; ~3× faster eviction, ~50% less KV-cache memory
- [`ai-inference-observability-platform`](https://github.com/ArchanaChetan07/ai-inference-observability-platform) — vLLM observability proxy (TTFT/TBT/E2E, Prometheus, OpenTelemetry); 56% lower P99 overhead, 3× SSE throughput
- [`KubeInfer`](https://github.com/ArchanaChetan07/KubeInfer) — Helm chart for multi-replica vLLM on Kubernetes with queue-depth autoscaling, validated on a 70B/4×A100 overlay

**Agentic systems** — multi-agent orchestration, tool use, and the guardrails that keep it honest.
- [`Multi-Agent-AI-Purchasing-System`](https://github.com/ArchanaChetan07/Multi-Agent-AI-Purchasing-System-with-Google-ADK-AMD-Instinct-GPUs) — cross-framework agent-to-agent purchasing flow (Google ADK, CrewAI, LangGraph) on AMD Instinct GPUs
- [`Multi-Agent-Incident-Response-System`](https://github.com/ArchanaChetan07/Multi-Agent-Incident-Response-System) — evidence-grounded incident triage with hallucination guarding and cost-aware LLM routing
- [`Python-MCP-Weather-Server`](https://github.com/ArchanaChetan07/Python-MCP-Weather-Server) · [`Real-time-Job-recommendation-system---MCP`](https://github.com/ArchanaChetan07/Real-time-Job-recommendation-system---MCP) — MCP tool servers

**Measurement and evaluation** — because a model or agent that "seems better" isn't the same as one that is.
- [`Multi-Agent-AI-System`](https://github.com/ArchanaChetan07/Multi-Agent-AI-System) — deterministic eval harness for a plan→route→observe→revise agent loop, with documented failure modes
- [`ab-test-guardrail-metrics`](https://github.com/ArchanaChetan07/ab-test-guardrail-metrics) — guardrail framework with SRM gating and pre-registered metrics, validated against real case studies
- [`Causal-Inference-Toolkit-for-Product-Metrics`](https://github.com/ArchanaChetan07/Causal-Inference-Toolkit-for-Product-Metrics) — DiD, synthetic control, and BSTS with ground-truth validation

**Semiconductor tooling** — RTL parsing, verification automation, and LLM-assisted design workflows.
- `rtlrag` — tree-sitter-based Verilog/SystemVerilog parser grounding an internal RAG system for design engineers
- RISC-V verification flow — Verilator + Spike golden-reference harness with automated signature-mismatch triage, adopted org-wide

---

### Tools I work with

![Python](https://img.shields.io/badge/-Python-3776AB?style=flat-square&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/-PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![CUDA](https://img.shields.io/badge/-CUDA-76B900?style=flat-square&logo=nvidia&logoColor=white)
![Kubernetes](https://img.shields.io/badge/-Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![Docker](https://img.shields.io/badge/-Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![FastAPI](https://img.shields.io/badge/-FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/-PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/-Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![LangChain](https://img.shields.io/badge/-LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white)
![Prometheus](https://img.shields.io/badge/-Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/-Grafana-F46800?style=flat-square&logo=grafana&logoColor=white)
![AWS](https://img.shields.io/badge/-AWS-232F3E?style=flat-square&logo=amazonaws&logoColor=white)

---

**M.S. Applied Data Science**, University of San Diego (GPA 3.9) · **NVIDIA Certified**, AI Infrastructure & Operations

📫 Reach me at [apatil@sandiego.edu](mailto:apatil@sandiego.edu) or [LinkedIn](https://linkedin.com/in/archanasureshpatil)
