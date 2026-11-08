# L5 Narrow / L2 General Classification — K_PRIVAIT
**Platform:** Anticloud | **Tier:** TIER_6_SECURITY_EVAL | **PAX:** 27B
**IP:** USPTO pending 2026, Anticloud FZ LLE, 0-1.gg | **License:** Apache-2.0

## L5 Narrow
K_PRIVAIT detects and protects PII in Anticloud data pipelines: scanning AIOSS chain entries, inference logs, and training data for unintended PII leakage. Narrow scope: Anticloud data privacy validation.

## L2 General
L2 General: K_PRIVAIT's PII detection protects all tiers. TIER_7 clinical data and TIER_9 user interaction logs both pass through K_PRIVAIT PII scanning before storage or AIOSS chaining.

## PAX 27B Integration
PAX 27B assists with context-aware PII detection: presidio identifies structural PII (SSN, email); PAX identifies contextual PII (indirect patient identifiers) that rule-based systems miss.

## AIOSS Audit Chain
Every privacy scan (input hash + PII detections hash + redacted output hash + risk level) is chained: H_n = SHA3-256(H_{n-1} || entry_hash_n || timestamp_n).
Offline-verifiable, tamper-evident, zero cloud dependency.

## Regulatory / Compliance
GDPR Art. 25/32 (privacy by design). HIPAA Safe Harbor. ISO 27701 (privacy management).
