# Deploy Guide — K_PRIVAIT
**Tier:** TIER_6_SECURITY_EVAL | **Stack:** Python 3.11, presidio (PII detection), PAX 27B, AIOSS_FORMAT
**Air-gap capable after initial setup.**

## Prerequisites
Python 3.11+, presidio-analyzer 2.2+, PAX 27B for contextual detection.

## Environment
4GB RAM. CPU for presidio. GPU for PAX contextual analysis.

## AIOSS Integration
```bash
aioss init --module K_PRIVAIT --output ./k_privait.aioss
aioss append --chain ./k_privait.aioss --payload ./output.bin --module K_PRIVAIT
aioss verify --chain ./k_privait.aioss
```

## Air-Gap Setup
```bash
pip download -r requirements.txt -d ./wheels/
pip install --no-index --find-links ./wheels/ -r requirements.txt
```

## PAX 27B Harness Wiring
```python
from anticloud_pax import PAXHarness
harness = PAXHarness(
    model_path="./pax-27b-q4.gguf",
    module="K_PRIVAIT",
    aioss_chain="./K_PRIVAIT.aioss",
    classification="L5_NARROW_L2_GENERAL"
)
result = harness.process(input_data)
```

## Verification
```bash
aioss verify --chain ./K_PRIVAIT.aioss --verbose
python -m K_PRIVAIT.tests.smoke
```
