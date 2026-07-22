<h1 align="center">Archana Suresh Patil</h1>

<p align="center">
  <b>Developer Infrastructure&nbsp;·&nbsp;CI, Test &amp; Release Systems for GPU and Inference Workloads</b>
</p>

<p align="center">
  I build the systems that let other engineers ship performance-critical GPU code with confidence:<br/>
  release-blocking correctness gates, test harnesses that keep GPU kernels verifiable on CPU-only CI,<br/>
  and the observability layer underneath LLM serving.
</p>

<p align="center">
  <a href="https://linkedin.com/in/archanasureshpatil"><img src="https://img.shields.io/badge/LinkedIn-archanasureshpatil-0A66C2?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="mailto:apatil@sandiego.edu"><img src="https://img.shields.io/badge/Email-apatil%40sandiego.edu-D14836?style=flat-square&logo=gmail&logoColor=white" alt="Email"></a>
  <img src="https://img.shields.io/badge/Location-Sunnyvale,%20CA-555555?style=flat-square&logo=googlemaps&logoColor=white" alt="Sunnyvale, CA">
  <img src="https://img.shields.io/badge/NVIDIA%20Certified-AI%20Infrastructure%20%26%20Operations-76B900?style=flat-square&logo=nvidia&logoColor=white" alt="NVIDIA Certified">
</p>

---

## Open source

Contributing to **[vLLM](https://github.com/vllm-project/vllm)** — the inference engine behind a large share of production LLM serving.

| Pull request | What it does | Status |
| :--- | :--- | :--- |
| **[#49366](https://github.com/vllm-project/vllm/pull/49366)**<br/>`[Bugfix]` | Aria produces garbage output at `tensor_parallel_size > 1`. Root-caused a **double all-reduce** of shared-expert output: the `MoERunner` contract requires unreduced per-rank partial sums, but Aria built its MLP without `reduce_results=False`. Audited all nine other in-tree MoE models to establish the invariant and confirm Aria was the sole outlier. **Fix is 3 lines.** | Open, under review |
| **[#48999](https://github.com/vllm-project/vllm/pull/48999)**<br/>`[Model]` | Adds **MiniCPM-SALA** — a 9.5B, 32-layer hybrid model (24 gated-linear "Lightning" attention layers + 8 GQA that switch to InfLLM-V2 block-sparse at long context). +1,630 lines, 34 CPU-only tests, greedy-token output **identical to the HuggingFace reference** on A100, TP=1/2/4 engine parity. | Open, under review |

Validation logs, compatibility matrix, and one-command reproduction scripts: **[vLLM-HybridAttn](https://github.com/ArchanaChetan07/vLLM-HybridAttn)**

---

## How I think about testing GPU code

Custom kernels are hard to test because the hardware is scarce and CI runners don't have it. My pattern across every kernel project:

**Write a NumPy reference implementation first, make it the correctness oracle, then gate the kernel against it bit-exactly — and dispatch CPU/GPU so the suite runs everywhere.**

The result is that contributors without a GPU can still verify correctness, and GPU scheduling stops being a source of flaky CI failures.

| Project | The gate | Measured |
| :--- | :--- | :--- |
| **[INT4 KV-Cache Quantization + Fused Flash-Attention](https://github.com/ArchanaChetan07/INT4-KV-Cache-Quantization-with-Fused-Flash-Attention-CUDA-Kernels-for-LLM-Serving)**<br/><sub>CUDA · Triton · PyTorch</sub> | 48 tests run with **no GPU**, 50 on hardware; Triton port validated in CI on CPU runners via interpreter mode | 0.000% quantizer bin disagreement · attention MAE 3.1e-8 · 3.98× KV compression · 3.9× kernel speedup |
| **[CUDA Speculative Decoding Optimizer](https://github.com/ArchanaChetan07/CUDA-Accelerated-Speculative-Decoding-Optimizer-for-LLM-Inference-PyTorch-vLLM-)**<br/><sub>CUDA · PyTorch</sub> | Six kernels each gated by **bit-exact equality vs NumPy**, including tie-breaking behavior | 31/31 on GPU · 29 on CPU-only runners |
| **[GPU Memory-Aware Request Scheduler](https://github.com/ArchanaChetan07/GPU-Memory-Aware-Request-Scheduler-with-KV-Cache-Offloading-for-Multi-Tenant-LLM-Serving)**<br/><sub>CUDA · SLA scheduling</sub> | **Bit-exact** gather → D2H → H2D → scatter round-trip gate | Swap-out 0.62 ms / swap-in 0.50 ms per 4 MB · admit rate 31.3% → 100% |
| **[PagedKV-Fusion](https://github.com/ArchanaChetan07/PagedKV-Fusion-Custom-CUDA-Kernels-for-KV-Cache-Eviction-Quantized-Paged-Attention)**<br/><sub>CUDA · INT8 paged attention</sub> | Reference-validated eviction scoring + quantized decode attention | Eviction 1.71 ms → 0.56 ms at 16K blocks (~3×) · ~50% KV memory |

---

## Developer productivity & reliability

- **[Real-Time Feature Store](https://github.com/ArchanaChetan07/Real-Time-Feature-Store-for-ML-Serving)** — a production-readiness audit that surfaced **five real concurrency bugs**, each reproduced with measurements and each given a permanent regression test. Parquet read-modify-write lost 174/200 records under 8 concurrent writers; every worker replica consumed every partition; online store applied last-write-wins by arrival order instead of `event_time`.
- **[AI Inference Observability Platform](https://github.com/ArchanaChetan07/ai-inference-observability-platform)** — FastAPI proxy exposing per-request **TTFT / TBT / E2E** for vLLM without forking the engine. P99 finalize overhead 46.1 µs → 20.1 µs (56%), SSE fast path 670 → 2,030 ops/sec. Publishes the proxy's *own* overhead cost alongside the wins.
- **[Agentic Verification Triage System](https://github.com/ArchanaChetan07/Agentic-Verification-Triage-System)** — automated regression-failure triage: parses logs into failure signatures, clusters related failures, drafts prioritized bugs, runs a critic pass to suppress false positives. Includes tests asserting that generated drafts are labeled non-LLM and that unavailable seeds stay `null` rather than being fabricated.
- **[KubeInfer](https://github.com/ArchanaChetan07/KubeInfer)** — production Helm chart for multi-replica vLLM on Kubernetes: session-affinity routing for KV reuse, **queue-depth autoscaling on `vllm:num_requests_waiting`** rather than CPU, NetworkPolicy, RBAC, 12 Prometheus alert rules, runbooks.
- **[LLM-HDL-Bench](https://github.com/ArchanaChetan07/-LLM-HDL-Bench-Verilog-RTL-Validation-Framework)** — 46-module SystemVerilog benchmark requiring agreement from **two independent tools** (Yosys + Icarus) before a result counts. Reports 46/46 post-fix *and* 45/46 with the human fix reverted.

---

## Measurement & causal evaluation

Because "seems better" and "is better" are different claims.

- **[A/B Test Guardrail Metrics](https://github.com/ArchanaChetan07/ab-test-guardrail-metrics)** — SRM gating, pre-registered metrics, Holm correction validated against the statsmodels reference. Applied to three real public experiments producing three different failure modes: a correctly-blocked regression, an honest "inconclusive," and a data-quality bug SRM alone could not detect.
- **[Toxic Content Prevalence & Intervention Impact](https://github.com/ArchanaChetan07/Toxic-Content-Prevalence-and-Intervention-Impact-Measurement-Platform)** — weighted difference-in-differences on **45.6M real Reddit comments**. Reports the label-noise sensitivity that *exceeds* the point estimate, rather than burying it.
- **[Causal Inference Toolkit](https://github.com/ArchanaChetan07/Causal-Inference-Toolkit-for-Product-Metrics)** — DiD, Synthetic Control, and BSTS behind one API with ground-truth validation and placebo tests. Surfaces **69% cross-method disagreement** instead of averaging incompatible answers.

---

## A note on the numbers

Every metric on this profile is reproducible from a committed artifact in the repository it belongs to. Where something is unmeasured, the repo says so — several READMEs explicitly retract earlier claims that turned out to be simulated or leakage-inflated, and label pending work as pending rather than done.

---

## Currently

**AI Engineer, Developer Tooling & Semiconductor Automation** at **SwanTech AI** — building an internal VS Code IDE wired to a self-hosted code model, a RISC-V RTL verification flow (Verilator + Spike golden reference), and a tree-sitter Verilog/SystemVerilog parser grounding an internal retrieval system for design engineers.

**M.S. Applied Data Science**, University of San Diego · GPA 3.9

---

## Tools

![Python](https://img.shields.io/badge/-Python-3776AB?style=flat-square&logo=python&logoColor=white)
![C++](https://img.shields.io/badge/-C++-00599C?style=flat-square&logo=cplusplus&logoColor=white)
![CUDA](https://img.shields.io/badge/-CUDA-76B900?style=flat-square&logo=nvidia&logoColor=white)
![Triton](https://img.shields.io/badge/-Triton-4B32C3?style=flat-square)
![PyTorch](https://img.shields.io/badge/-PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![vLLM](https://img.shields.io/badge/-vLLM-111111?style=flat-square)
![pytest](https://img.shields.io/badge/-pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/-GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![Docker](https://img.shields.io/badge/-Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/-Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![Helm](https://img.shields.io/badge/-Helm-0F1689?style=flat-square&logo=helm&logoColor=white)
![Prometheus](https://img.shields.io/badge/-Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/-Grafana-F46800?style=flat-square&logo=grafana&logoColor=white)
![OpenTelemetry](https://img.shields.io/badge/-OpenTelemetry-000000?style=flat-square&logo=opentelemetry&logoColor=white)
![FastAPI](https://img.shields.io/badge/-FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Terraform](https://img.shields.io/badge/-Terraform-7B42BC?style=flat-square&logo=terraform&logoColor=white)
![AWS](https://img.shields.io/badge/-AWS-232F3E?style=flat-square&logo=amazonaws&logoColor=white)
![Verilog](https://img.shields.io/badge/-Verilog%2FSystemVerilog-B2B7F8?style=flat-square)

---

<p align="center">
  <sub>Open to developer-infrastructure and inference-systems roles ·
  <a href="mailto:apatil@sandiego.edu">apatil@sandiego.edu</a> ·
  <a href="https://linkedin.com/in/archanasureshpatil">LinkedIn</a></sub>
</p>
