# From Amazon to production in 17 days: a 128 GB AI workstation serving real agents

**Juan Manuel Fraga Sastrías** · ORCID [0000-0002-9255-278X](https://orcid.org/0000-0002-9255-278X) · [docfraga.com](https://www.docfraga.com)

Technical note · version 1.0 · 2026-10-07 · License [CC BY 4.0](LICENSE)

## Abstract

A physician's field report on standing up local LLM inference for production health-care agents. An ASUS Ascent GX10 (NVIDIA GB10 Grace Blackwell, 128 GB unified memory) went from the box to serving a 35-billion-parameter mixture-of-experts model (Qwen3.6-35B, NVFP4, vLLM) in 17 days. The note reports measured latency and throughput, the inference-engine configuration and why each option was chosen, the failure modes seen in production and their mitigations, the routing layer that lets agents switch between local and cloud models, and how models are selected through the author's own head-to-head evaluation arenas. A technical appendix details the memory budget, benchmark methodology, vLLM flags, and the arenas run.

## Files

| File | Language |
|---|---|
| [`local-ai-workstation-en.pdf`](local-ai-workstation-en.pdf) | English |
| [`local-ai-workstation-es.pdf`](local-ai-workstation-es.pdf) | Español |

Web versions: [English](https://www.docfraga.com/en/whitepapers/gx10-17-dias) · [Español](https://www.docfraga.com/whitepapers/gx10-17-dias)

## How to cite

Fraga-Sastrías JM. *From Amazon to production in 17 days: a 128 GB AI workstation serving real agents*. Technical note, version 1.0. 2026.
A DOI will be listed here once the release is archived in Zenodo.
