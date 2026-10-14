# Students — CORE_BIOIMAGE_IO_PYTHON

**Project:** CORE_BIOIMAGE_IO_PYTHON  
**Category:** SCIENTIFIC_LAB  
**Upstream:** https://github.com/bioimage-io/core-bioimage-io-python  
**Pinned commit:** `31703b23e9d666a94bedab248411d95348a18ab3`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `d9dcc951c9b29ad2df8733b0c6e53f98c8aa47d00177535cad948be51e8c85c9`  
**Date:** October 2026

## What this project gives you

A complete worked example of offline-first packaging with a cryptographic audit
chain: source pinned at `31703b23e9d666a94bedab248411d95348a18ab3`, a 16-check assurance suite, an evidence register
with per-check hashes, and an AIOSS ledger chain ending at `d9dcc951c9b29ad2df8733b0c6e53f98c8aa47d00177535cad948be51e8c85c9`.

## Learn by verifying

```
python tools/run_bench.py --out BENCH.json
```

Then take any row from `ISOLATED_LAB_RESULTS/03_Result_Register.md`, recompute
the SHA3-256 of its evidence file, and confirm it matches. If it does not match,
the record has been altered — that is the whole point of the chain.

## Licence

Apache 2.0 terms apply to study and teaching use.
