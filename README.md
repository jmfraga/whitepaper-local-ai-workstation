# From Amazon to production in 17 days: a 128 GB AI workstation serving real agents

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.23213603.svg)](https://doi.org/10.5281/zenodo.23213603)

**Juan Manuel Fraga Sastrías** · ORCID [0000-0002-9255-278X](https://orcid.org/0000-0002-9255-278X) · [docfraga.com](https://www.docfraga.com)

Technical note · version 1.2 · 2026-10-07 · License [CC BY 4.0](LICENSE)

## Abstract

A physician's field report on standing up local LLM inference for production health-care agents. An ASUS Ascent GX10 (NVIDIA GB10 Grace Blackwell, 128 GB unified memory) went from the box to serving a 35-billion-parameter mixture-of-experts model (Qwen3.6-35B, NVFP4, vLLM) in 17 days. The note reports measured latency and throughput, the inference-engine configuration and why each option was chosen, the failure modes seen in production and their mitigations, the routing layer that lets agents switch between local and cloud models, and how models are selected through the author's own head-to-head evaluation arenas. A technical appendix details the memory budget, benchmark methodology, vLLM flags, and the arenas run.

## Files

| File | Language |
|---|---|
| [`local-ai-workstation-en.pdf`](local-ai-workstation-en.pdf) | English |
| [`local-ai-workstation-es.pdf`](local-ai-workstation-es.pdf) | Español |

### Arena reports (appendix, in Spanish)

Reports marked *reconstruction* were rebuilt afterwards from the notes taken on the day of the test; the original report and raw data were not kept, and each one says so at the top. Oncology evaluations are excluded because their data belong to a study under review.

| Date | Arena | File |
|---|---|---|
| 2026-08-11 | Tool use: Qwen3.6-35B-A3B vs Muse Glimmer 30B *(reconstruction)* | [`arena-2026-08-11-tooluse-qwen-vs-glimmer.pdf`](arena-reports/arena-2026-08-11-tooluse-qwen-vs-glimmer.pdf) |
| 2026-08-11 | Qwen3.6-35B-A3B vs Nemotron 3.5 Lightning 30B-A3B *(reconstruction)* | [`arena-2026-08-11-qwen-vs-nemotron.pdf`](arena-reports/arena-2026-08-11-qwen-vs-nemotron.pdf) |
| 2026-08-11 | General model vs a “healthcare” fine-tune *(reconstruction)* | [`arena-2026-08-11-generalista-vs-finetune-salud.pdf`](arena-reports/arena-2026-08-11-generalista-vs-finetune-salud.pdf) |
| 2026-08-14 | Five sampling profiles, same model | [`arena-2026-08-14-perfiles-muestreo.pdf`](arena-reports/arena-2026-08-14-perfiles-muestreo.pdf) |
| 2026-08-14 | Qwen3.6-35B-A3B (MoE) vs Qwen3.8-27B (dense), with a 2026-09-18 rematch *(reconstruction)* | [`arena-2026-08-14-qwen36-vs-qwen38.pdf`](arena-reports/arena-2026-08-14-qwen36-vs-qwen38.pdf) |
| 2026-09-18 | Ternary Bonsai 2 (1.72 bits) vs Qwen3.8-27B and Qwen3.6-35B-A3B | [`arena-2026-09-18-bonsai2-vs-qwen.pdf`](arena-reports/arena-2026-09-18-bonsai2-vs-qwen.pdf) |
| 2026-09-28 | Does this turn trigger an irreversible action? Three classifiers | [`arena-2026-09-28-clasificador-irreversibles.pdf`](arena-reports/arena-2026-09-28-clasificador-irreversibles.pdf) |
| 2026-10-03 | Browser agent: local Qwen3.6 vs Sonnet as the brain | [`arena-2026-10-03-brazo-navegador.pdf`](arena-reports/arena-2026-10-03-brazo-navegador.pdf) |
| 2026-10-05 | Agentic safety: Qwen3.6-35B-A3B vs its abliterated version | [`arena-2026-10-05-seguridad-ablacion.pdf`](arena-reports/arena-2026-10-05-seguridad-ablacion.pdf) |

Web versions: [English](https://www.docfraga.com/en/whitepapers/gx10-17-dias) · [Español](https://www.docfraga.com/whitepapers/gx10-17-dias)

## How to cite

Fraga-Sastrías JM. *From Amazon to production in 17 days: a 128 GB AI workstation serving real agents*. Technical note, version 1.2. 2026.
https://doi.org/10.5281/zenodo.23213603

- All versions (concept DOI, always resolves to the latest): [10.5281/zenodo.23213603](https://doi.org/10.5281/zenodo.23213603)
- Version 1.1: [10.5281/zenodo.23214666](https://doi.org/10.5281/zenodo.23214666)
- Version 1.0: [10.5281/zenodo.23213604](https://doi.org/10.5281/zenodo.23213604)

## Changelog

- **1.2** (2026-10-07): Adds appendix 7, «Arena reports»: the downloadable report of each arena behind the model decisions (nine PDFs in `arena-reports/`, in Spanish; four are labelled reconstructions). Report texts follow the same redaction rules as the note (no internal agent or machine names, no locations or network details).
- **1.1** (2026-10-07): Adds the agentic-safety arena (2026-10-05): standard vs abliterated (Heretic) Qwen3.6-35B-A3B in a clean pair; critical failures 40 % → 77 %, with permissions (0/20 → 17/20) and clinical confidentiality (0/20 → 15/20) breaking. New third lesson in the arenas section; DOI printed in the header.
- **1.0** (2026-10-07): first release.
