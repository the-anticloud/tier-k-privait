# HF_Leaderboard_Lab_Results

**Project:** `K_PRIVAIT`  
**Tier:** `TIER_6_SECURITY_EVAL`  
**Slug:** `microsoft/presidio`  
**Commit:** `d4ccc6bcb6b6`  
**Run:** `2026-09-30T15:07:07.146295+00:00`  

## Isolation Environment

| Field | Value |
| ----- | ----- |
| Platform | `win32` |
| Python | `3.12.10` |
| HF model | `distilbert-base-uncased` |
| HF load time | `4.42s` |
| Inference device | `cpu` |

## Results

**Framework:** [HuggingFace Open LLM Leaderboard (proxy via distilbert-base-uncased)](https://huggingface.co/docs/leaderboards/en/open_llm_leaderboard/archive)

**Model used:** `distilbert-base-uncased`

### Inference Latency (Classification)

| Metric | Value |
| ------ | ----- |
| Avg latency | **49.71 ms** |
| Min latency | 38.67 ms |
| Max latency | 61.97 ms |
| Samples | 5 |

### Real Tokenization Results

| Field | Value |
| ----- | ----- |
| Token count | **35** |
| Tokenization latency | 1.0 ms |
| Classification label | `LABEL_0` |
| Classification score | 0.5877 |
| Classification latency | 67.93 ms |
| Status | **PASS** |

**Input text tokenized:**
```
K_PRIVAIT (microsoft/presidio) — 917 files, 69351 source lines, licence MIT, primary language ['Python']
```

**First 20 tokens:**
```
['[CLS]', 'k', '_', 'pri', '##va', '##it', '(', 'microsoft', '/', 'pre', '##si', '##dio', ')', '—', '91', '##7', 'files', ',', '69', '##35']
```

> Full MMLU/HellaSwag/TruthfulQA/ARC/Winogrande/GSM8K require dedicated GPU.
> These results are CPU inference proxy metrics using distilbert-base-uncased.

---
_Anticloud Benchmark Suite — isolation log — 2026-09-30T15:07:07.146295+00:00_