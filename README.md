# PUMIS — Replication Archive (SMR submission)

Anonymous replication archive accompanying the manuscript *Diagnosing and Correcting Partition-Uncertainty-Induced Inference in Two-Step Migration Systems Analysis*.

## What this archive contains

- `config.yaml` — the single locked parameter source (all `locked` parameters preregistered).
- `logs/` — three append-only execution logs: progress, decisions (incl. data-incident disclosure), and exploratory deviations. These logs constitute the audit trail required by the preregistration.
- OSF preregistration: https://osf.io/y2n9c/ (registered 2026-09-28; exploratory executions preceding registration are labeled method development in the logs).
- Full pipeline scripts, derived data, and the `pumis` package will be deposited at Zenodo with a versioned DOI upon acceptance; they are available to reviewers on request through the editor.

## One-command reproduction (post-Zenodo)

```
python code/download_all.py     # zero-application data acquisition
python code/t3_sptd_tensor.py   # tensor construction
Rscript code/t4_t5_sptd.R       # stage-1 + gate
```

Global seed: 42. Runtimes and environment versions are pinned in `config.yaml` (environment section).
