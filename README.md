<div align="center">

[![Typing SVG](https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=700&size=26&pause=1000&color=6E40C9&center=true&vCenter=true&width=750&lines=Archana+Suresh+Patil;Platform+%26+MLOps+Engineer;LLMs+%C2%B7+Kubernetes+%C2%B7+NVIDIA+GPU+%C2%B7+AI+Infra;Open+to+Full-Time+Roles+%E2%80%94+No+Sponsorship+Needed)](https://git.io/typing-svg)

<br/>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/archana-suresh-patil-792213245)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/ArchanaChetan07)
[![Email](https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:apatil@sandiego.edu)
[![Location](https://img.shields.io/badge/Sunnyvale%2C%20CA-No%20Sponsorship%20Needed-2ea44f?style=for-the-badge&logo=googlemaps&logoColor=white)](#)

</div>

---

## 👩‍💻 About Me

**Platform & MLOps Engineer** with a focus on production AI infrastructure — deploying, scaling, and observing LLMs on Kubernetes with NVIDIA GPUs.

- 🎓 MS Data Science · University of San Diego · GPA 3.9 · Dec 2025
- 🚀 Built **KubeInfer** — production-grade LLM inference platform (vLLM · Helm · NVIDIA GPU · GitOps)
- 🤖 NLP researcher — BERT-based emotion detection and crisis support (EmotiCare)
- 🔍 ML practitioner — fraud detection, image classification, time-series forecasting
- 📍 Sunnyvale, CA · Open to full-time · No sponsorship needed
- 📬 apatil@sandiego.edu

**Open to:** MLOps Engineer · ML Engineer · Platform Engineer · AI Infrastructure · Data Scientist · Founding Engineer (AI)

---

## 🏆 Achievement Stickers

<div align="center">

| 🥇 | Achievement | Stack |
|:---:|:---|:---|
| ![GPU](https://img.shields.io/badge/GPU%20Infra%20Engineer-Production%20vLLM%20on%20NVIDIA%20GPU-76B900?style=flat-square&logo=nvidia&logoColor=white) | Deployed production-grade LLM inference on NVIDIA GPUs with PagedAttention & continuous batching | `vLLM` `CUDA` `DCGM` |
| ![K8s](https://img.shields.io/badge/Kubernetes%20Architect-Helm%20%7C%20HPA%20%7C%20GitOps-326CE5?style=flat-square&logo=kubernetes&logoColor=white) | Designed full Helm chart with queue-depth autoscaling, PDB, RBAC, and NetworkPolicy | `Helm` `HPA` `ArgoCD` |
| ![MLOps](https://img.shields.io/badge/MLOps%20Builder-CI%2FCD%20%7C%20Observability%20%7C%20Alerts-FF6F00?style=flat-square&logo=prometheus&logoColor=white) | End-to-end MLOps pipeline: lint → test → trivy scan → staged deploy with rollback | `Prometheus` `Grafana` `GitHub Actions` |
| ![NLP](https://img.shields.io/badge/NLP%20Researcher-BERT%20%7C%20Emotion%20Detection%20%7C%20Crisis%20AI-8B5CF6?style=flat-square&logo=huggingface&logoColor=white) | Built BERT-based empathy engine with real-time emotional crisis detection | `BERT` `Transformers` `PyTorch` |
| ![Security](https://img.shields.io/badge/Security%20First-Zero--Trust%20NetworkPolicy%20%7C%20RBAC-DC143C?style=flat-square&logo=shieldsdotio&logoColor=white) | Hardened K8s cluster: least-privilege RBAC, deny-all NetworkPolicy, Trivy image scanning | `RBAC` `PSS` `Trivy` |

</div>

---

## 🚀 Featured Project — KubeInfer

> **Production-grade LLM inference platform** · Kubernetes · NVIDIA GPU · vLLM · Helm · GitOps · Prometheus

```
Internet ──► nginx Ingress (TLS) ──► Request Router ──► vLLM Engine × N
                                          │                    │
                                     Session HPA          NVIDIA GPU
                                 (vllm:num_requests_waiting) PagedAttention
                                                              │
                                                    Shared PVC (model cache)
```

[![KubeInfer](https://img.shields.io/badge/KubeInfer-View%20on%20GitHub-181717?style=for-the-badge&logo=github)](https://github.com/ArchanaChetan07/KubeInfer)
![Stars](https://img.shields.io/github/stars/ArchanaChetan07/KubeInfer?style=for-the-badge&color=6E40C9)
![Last Commit](https://img.shields.io/github/last-commit/ArchanaChetan07/KubeInfer?style=for-the-badge&color=76B900)
![Language](https://img.shields.io/github/languages/top/ArchanaChetan07/KubeInfer?style=for-the-badge&color=326CE5)

**What makes it production-grade:**
- 🎯 HPA on `vllm:num_requests_waiting` — queue depth signal, not CPU (meaningless for GPU workloads)
- 🔒 Zero-trust NetworkPolicy · Least-privilege RBAC · Pod Security Standards · Trivy scanning
- 📊 12 Alertmanager rules · 10-panel Grafana dashboard · NVIDIA DCGM GPU metrics
- 🔄 GitHub Actions: lint → helm-unittest → kubeconform → trivy → staged deploy → smoke tests
- 🧱 `dev / staging / prod` Helm values · PodDisruptionBudget · ReadWriteMany model cache PVC

**Keywords:** `kubernetes` `mlops` `llmops` `vllm` `nvidia-gpu` `helm` `gitops` `prometheus` `grafana` `platform-engineering` `inference` `gpu`

---

## 🤖 AI & ML Projects

| Project | What it does | Stack | Result |
|---|---|---|---|
| [EmotiCare](https://github.com/ArchanaChetan07/EmotiCare_-AI-Powered-Mental-Health-Assistant) | AI mental health assistant — NLP + emotion detection for empathetic crisis support | BERT · PyTorch · Transformers | ⭐ 1 star |
| [Fraud Detection](https://github.com/ArchanaChetan07/Credit-Card-Transactions-Fraud-Detection-Project) | Credit card fraud detection on imbalanced transaction data (0.17% fraud rate) | XGBoost · CatBoost · SMOTE | 86% recall |
| [Apparel Classification](https://github.com/ArchanaChetan07/Apparel-Image-Classification-with-WideResNet) | Fashion image classification with deep learning and transfer learning | WideResNet · PyTorch | Transfer learning |
| [Traffic Forecasting](https://github.com/ArchanaChetan07/Metro-Interstate-Traffic-Volume-Forecasting) | Metro interstate traffic volume forecasting using deep learning | LSTM · TensorFlow · Time-series | Highway data |

---

## 🛠 Tech Stack

<div align="center">

**AI Infrastructure & MLOps**

![vLLM](https://img.shields.io/badge/vLLM-Inference%20Engine-FF6B35?style=flat-square)
![NVIDIA](https://img.shields.io/badge/NVIDIA-GPU%20Operator%20%7C%20DCGM-76B900?style=flat-square&logo=nvidia&logoColor=white)
![CUDA](https://img.shields.io/badge/CUDA-Acceleration-76B900?style=flat-square&logo=nvidia&logoColor=white)
![HuggingFace](https://img.shields.io/badge/HuggingFace-Transformers%20%7C%20Models-FFD21E?style=flat-square&logo=huggingface&logoColor=black)
![MLflow](https://img.shields.io/badge/MLflow-Experiment%20Tracking-0194E2?style=flat-square&logo=mlflow&logoColor=white)

**Platform & Orchestration**

![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![Helm](https://img.shields.io/badge/Helm-0F1689?style=flat-square&logo=helm&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![ArgoCD](https://img.shields.io/badge/ArgoCD-EF7B4D?style=flat-square&logo=argo&logoColor=white)
![MetalLB](https://img.shields.io/badge/MetalLB-LoadBalancer-326CE5?style=flat-square)

**Observability**

![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white)
![Alertmanager](https://img.shields.io/badge/Alertmanager-E6522C?style=flat-square&logo=prometheus&logoColor=white)

**ML & Data Science**

![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikit-learn&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-189ABE?style=flat-square)
![BERT](https://img.shields.io/badge/BERT-NLP-8B5CF6?style=flat-square)

**CI/CD & Security**

![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![Trivy](https://img.shields.io/badge/Trivy-Image%20Scanning-1904DA?style=flat-square)
![cert-manager](https://img.shields.io/badge/cert--manager-TLS%20Automation-003B8E?style=flat-square)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)

</div>

---

## 📈 GitHub Stats

<div align="center">

<img height="160" src="https://github-readme-stats.vercel.app/api?username=ArchanaChetan07&show_icons=true&theme=tokyonight&hide_border=true&count_private=true" />
<img height="160" src="https://github-readme-stats.vercel.app/api/top-langs/?username=ArchanaChetan07&layout=compact&theme=tokyonight&hide_border=true" />

</div>

<div align="center">

[![GitHub Streak](https://streak-stats.demolab.com?user=ArchanaChetan07&theme=tokyonight&hide_border=true)](https://git.io/streak-stats)

</div>

---

## 🎖 GitHub Achievements

<div align="center">

![Profile Views](https://komarev.com/ghpvc/?username=ArchanaChetan07&style=flat-square&color=6E40C9&label=Profile+Views)
[![GitHub followers](https://img.shields.io/github/followers/ArchanaChetan07?style=flat-square&color=6E40C9&label=Followers)](https://github.com/ArchanaChetan07)

| Badge | Status | How to earn |
|:---:|:---|:---|
| 🦈 Pull Shark | ✅ Earned | Merged PRs — already unlocked! |
| 🌟 Starstruck | 🔄 In progress | Need 16 stars on KubeInfer |
| ⚡ Quickdraw | 🔄 In progress | Close an issue within 5 min of opening |

</div>

---

## 💬 What I Build

**Platform & MLOps Engineer** — I close the gap between a working notebook and a model serving production traffic.

Most teams can train a model. Few can serve it reliably at scale. I build the layer in between:

- **GPU-aware Kubernetes scheduling** — right model on right hardware, every time
- **Inference-specific autoscaling** — scale on queue depth, not CPU
- **Observability that actually pages** — 12 alerts covering TTFT, KV cache, preemptions, HPA failures
- **GitOps workflows** — dev → staging → prod with smoke tests and rollback at every step
- **NLP systems** — BERT-based emotion detection, crisis classification, empathetic response generation

**Open to full-time roles in:** MLOps · ML Engineering · Platform Engineering · AI Infrastructure · Data Science · Founding Engineer (AI)

📍 Sunnyvale, CA · No sponsorship needed · Available Dec 2025
📬 apatil@sandiego.edu

---

<div align="center">
<sub>MS Data Science · University of San Diego · GPA 3.9 · Dec 2025 · Built with ☕ and a lot of kubectl</sub>
</div>
