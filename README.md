<div align="center">

<!-- Typing animation headline -->
[![Typing SVG](https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=700&size=28&pause=1000&color=6E40C9&center=true&vCenter=true&width=700&lines=Hey%2C+I'm+Archana+%F0%9F%91%8B;Platform+%26+MLOps+Engineer;Building+AI+Infrastructure+at+Scale;LLMs+%C2%B7+Kubernetes+%C2%B7+NVIDIA+GPUs)](https://git.io/typing-svg)

<br/>

<!-- Social badges -->
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/archanachetan07)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/ArchanaChetan07)
[![Email](https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:your@email.com)

</div>

---

## 🏆 Achievement Stickers

<div align="center">

| 🥇 | Achievement | Stack |
|:---:|:---|:---|
| ![GPU](https://img.shields.io/badge/GPU%20Infra%20Engineer-Production%20vLLM%20on%20NVIDIA%20A100-76B900?style=flat-square&logo=nvidia&logoColor=white) | Deployed production-grade LLM inference on NVIDIA GPUs with PagedAttention & continuous batching | `vLLM` `CUDA` `DCGM` |
| ![K8s](https://img.shields.io/badge/Kubernetes%20Architect-Helm%20%7C%20HPA%20%7C%20GitOps-326CE5?style=flat-square&logo=kubernetes&logoColor=white) | Designed a full Helm chart with queue-depth autoscaling, PDB, RBAC, and NetworkPolicy | `Helm` `HPA` `ArgoCD` |
| ![MLOps](https://img.shields.io/badge/MLOps%20Builder-CI%2FCD%20%7C%20Observability%20%7C%20Alerts-FF6F00?style=flat-square&logo=prometheus&logoColor=white) | Built end-to-end MLOps pipeline: lint → test → scan → staged deploy with rollback | `Prometheus` `Grafana` `GitHub Actions` |
| ![Security](https://img.shields.io/badge/Security%20First-Zero--Trust%20NetworkPolicy%20%7C%20RBAC-DC143C?style=flat-square&logo=shieldsdotio&logoColor=white) | Hardened K8s cluster with least-privilege RBAC, deny-all NetworkPolicy, and Trivy image scanning | `RBAC` `PSS` `Trivy` |
| ![Startup](https://img.shields.io/badge/Startup%20Engineer-0→1%20Platform%20Infrastructure-6E40C9?style=flat-square&logo=rocket&logoColor=white) | Built production AI infrastructure from scratch, designed for a founding team to ship fast | `Platform Eng` `MLOps` `AI Infra` |

</div>

---

## 🚀 Featured Project — KubeInfer

> **Production-grade LLM inference platform** · Kubernetes · NVIDIA GPU · vLLM · Helm · GitOps

```
Internet ──► nginx Ingress (TLS) ──► Request Router ──► vLLM Engine × N
                                          │                    │
                                     Session HPA          NVIDIA GPU
                                   (queue-depth)         PagedAttention
                                                              │
                                                    Shared PVC (model cache)
```

[![KubeInfer](https://img.shields.io/badge/KubeInfer-View%20on%20GitHub-181717?style=for-the-badge&logo=github)](https://github.com/ArchanaChetan07/KubeInfer)
![Stars](https://img.shields.io/github/stars/ArchanaChetan07/KubeInfer?style=for-the-badge&color=6E40C9)
![Last Commit](https://img.shields.io/github/last-commit/ArchanaChetan07/KubeInfer?style=for-the-badge&color=76B900)

**What makes it production-grade:**
- 🎯 HPA scales on `vllm:num_requests_waiting` (queue depth) — not CPU, which is meaningless for GPU workloads
- 🔒 Zero-trust NetworkPolicy · Least-privilege RBAC · Pod Security Standards
- 📊 12 Alertmanager rules · 10-panel Grafana dashboard · DCGM GPU metrics
- 🔄 GitHub Actions CI/CD: lint → helm-unittest → kubeconform → trivy → staged deploy with manual approval gate
- 🧱 `dev / staging / prod` Helm values — same chart, different constraints per environment

---

## 🛠 Tech Stack

<div align="center">

**AI Infrastructure**

![vLLM](https://img.shields.io/badge/vLLM-Inference%20Engine-FF6B35?style=flat-square)
![NVIDIA](https://img.shields.io/badge/NVIDIA-GPU%20Operator%20%7C%20DCGM-76B900?style=flat-square&logo=nvidia&logoColor=white)
![CUDA](https://img.shields.io/badge/CUDA-Acceleration-76B900?style=flat-square&logo=nvidia&logoColor=white)
![HuggingFace](https://img.shields.io/badge/HuggingFace-Models-FFD21E?style=flat-square&logo=huggingface&logoColor=black)

**Platform & Orchestration**

![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![Helm](https://img.shields.io/badge/Helm-0F1689?style=flat-square&logo=helm&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![ArgoCD](https://img.shields.io/badge/ArgoCD-EF7B4D?style=flat-square&logo=argo&logoColor=white)

**Observability**

![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white)
![Alertmanager](https://img.shields.io/badge/Alertmanager-E6522C?style=flat-square&logo=prometheus&logoColor=white)

**CI/CD & Security**

![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![Trivy](https://img.shields.io/badge/Trivy-Image%20Scanning-1904DA?style=flat-square)
![cert-manager](https://img.shields.io/badge/cert--manager-TLS%20Automation-003B8E?style=flat-square)

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

## 🎖 Badges I've Earned

<div align="center">

![Profile Views](https://komarev.com/ghpvc/?username=ArchanaChetan07&style=flat-square&color=6E40C9&label=Profile+Views)
[![GitHub followers](https://img.shields.io/github/followers/ArchanaChetan07?style=flat-square&color=6E40C9&label=Followers)](https://github.com/ArchanaChetan07)

<!-- GitHub Achievement badges (auto-awarded by GitHub) -->
<!--
  These appear automatically on your GitHub profile once earned:
  ⚡ Quickdraw      — Closed an issue/PR within 5 min of opening
  🦈 Pull Shark     — Opened PRs that got merged (×2 = bronze, ×16 = silver, ×128 = gold)
  🌟 Starstruck     — Created a repo with 16+ stars
  🏔 Arctic Code Vault — Contributed to the 2020 GitHub Arctic Vault
  ❤️ Sponsor        — Sponsored an open source contributor
-->

**Working toward:**

| Badge | Target | How |
|:---:|:---|:---|
| 🦈 Pull Shark | Merge 2 PRs into KubeInfer | Open a PR from a feature branch, merge it |
| 🌟 Starstruck | 16 stars on KubeInfer | Share on LinkedIn + MLOps communities |
| ⚡ Quickdraw | Close an issue within 5 min | Open + close a good-first-issue |

</div>

---

## 💬 What I'm Building

I'm a Platform / MLOps Engineer focused on **making LLMs run reliably in production**.

Most teams get an LLM working in a notebook, then struggle to serve it at scale.
I build the infrastructure layer that bridges that gap:
- GPU-aware Kubernetes scheduling
- Inference-specific autoscaling (queue depth, not CPU)
- Observability pipelines that catch OOM kills before users do
- GitOps workflows teams can actually maintain

**Open to:** Platform Engineering · MLOps · AI Infrastructure · Founding Engineer roles

---

<div align="center">
<sub>Built with ☕ and a lot of kubectl</sub>
</div>
