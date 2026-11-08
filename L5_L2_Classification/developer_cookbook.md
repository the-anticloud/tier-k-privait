# Developer Cookbook — K_PRIVAIT
**Stack:** Python 3.11, presidio (PII detection), PAX 27B, AIOSS_FORMAT
**Domain:** PrivAIT: privacy-preserving AI testing and PII detection for Anticloud

## PII detection and redaction
```python
from k_privait import PrivAITScanner

scanner = PrivAITScanner(
    pax_model="./pax-27b-q4.gguf",
    aioss_chain="./privait.aioss"
)

# Scan and redact
result = scanner.scan_and_redact(
    text="Patient John Smith (DOB: 1985-03-15, SSN: 123-45-6789) shows elevated theta"
)
print(f"PII found: {result.pii_entities}")
print(f"Redacted: {result.redacted_text}")
# "Patient [NAME] (DOB: [DATE], SSN: [SSN]) shows elevated theta"
print(f"Chain: {result.chain_hash}")
```

## Scan AIOSS chain for PII leakage
```python
leakage = scanner.scan_aioss_chain("./audit.aioss")
print(f"PII in chain: {leakage.found_pii}")
```

## AIOSS Chain Append
```python
import hashlib, time

def aioss_append(chain_path, payload: bytes, module_id: str):
    entry_hash = hashlib.sha3_256(payload).digest()
    ts = int(time.time_ns()).to_bytes(8, 'big')
    with open(chain_path, 'rb') as f:
        f.seek(-32, 2); prev_hash = f.read(32)
    new_hash = hashlib.sha3_256(prev_hash + entry_hash + ts).digest()
    with open(chain_path, 'ab') as f:
        f.write(ts + entry_hash + new_hash)
    return new_hash.hex()
```
