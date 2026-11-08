# Radon_Complexity_Lab_Results
**Project:** `K_PRIVAIT` | **Status:** `PASS` | **Run:** `2026-09-30T17:14:20.030944+00:00`

**Framework:** [Radon — Cyclomatic Complexity & Maintainability Index](https://radon.readthedocs.io/)

## Key Metrics

- **files_analyzed:** `10`
- **average_complexity:** `{'grade': 'A', 'score': 2.5238095238095237}`
- **complexity_grade:** `A`
- **complexity_score:** `2.5238095238095237`
- **mi_output:** `E:\fenta\Downloads\The Anticloud\TIER_6_SECURITY_EVAL\K_PRIVAIT\UPSTREAM\presidio-analyzer\app.py - A (51.57)
E:\fenta\D`

## Raw Output (first 50 lines)
```
E:\fenta\Downloads\The Anticloud\TIER_6_SECURITY_EVAL\K_PRIVAIT\UPSTREAM\presidio-analyzer\app.py
    C 37:0 Server - A (5)
    F 168:0 _exclude_attributes_from_dto - A (4)
    M 40:4 Server.__init__ - A (4)
    F 178:0 create_app - A (1)
E:\fenta\Downloads\The Anticloud\TIER_6_SECURITY_EVAL\K_PRIVAIT\UPSTREAM\presidio-analyzer\install_nlp_models.py
    F 88:0 _download_model - B (8)
    F 29:0 install_models - B (6)
    F 65:0 _install_models_from_nlp_config - A (4)
    F 107:0 _install_transformers_spacy_models - A (3)
E:\fenta\Downloads\The Anticloud\TIER_6_SECURITY_EVAL\K_PRIVAIT\UPSTREAM\presidio-anonymizer\app.py
    C 30:0 Server - A (2)
    F 115:0 create_app - A (1)
    M 33:4 Server.__init__ - A (1)
E:\fenta\Downloads\The Anticloud\TIER_6_SECURITY_EVAL\K_PRIVAIT\UPSTREAM\presidio-image-redactor\app.py
    C 32:0 Server - A (2)
    F 83:0 create_app - A (1)
    M 35:4 Server.__init__ - A (1)
E:\fenta\Downloads\The Anticloud\TIER_6_SECURITY_EVAL\K_PRIVAIT\UPSTREAM\scripts\zensical_build.py
    F 243:0 main - B (9)
    F 170:0 _rewrite_links - A (4)
    F 115:0 _stage_docs - A (3)
    F 129:0 _convert_notebooks - A (3)
    F 209:0 _write_generated_config - A (3)
    F 83:0 _ignore_python_name - A (1)
    F 92:0 _collect_notebooks - A (1)
    C 74:0 _TolerantLoader - A (1)
E:\fenta\Downloads\The Anticloud\TIER_6_SECURITY_EVAL\K_PRIVAIT\UPSTREAM\docs\samples\python\example_custom_lambda_anonymizer.py
    F 8:0 reverse_string - A (1)
    F 13:0 anonymize_reverse_lambda - 
```

---
_Anticloud Independent Benchmark — 2026-09-30T17:14:20.030944+00:00_