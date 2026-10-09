# Educators — CORE_BIOIMAGE_IO_PYTHON

**Project:** CORE_BIOIMAGE_IO_PYTHON  
**Category:** SCIENTIFIC_LAB  
**Upstream:** https://github.com/bioimage-io/core-bioimage-io-python  
**Pinned commit:** `31703b23e9d666a94bedab248411d95348a18ab3`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `d9dcc951c9b29ad2df8733b0c6e53f98c8aa47d00177535cad948be51e8c85c9`  
**Date:** October 2026

## Teaching with CORE_BIOIMAGE_IO_PYTHON

The project is usable as a worked example of offline-first packaging with a
cryptographic audit chain. It ships with the assurance suite, the evidence
register and the ledger, so students can verify claims rather than take them on
faith.

## Suggested exercises

1. Run `python tools/run_bench.py --out BENCH.json` and read the 16 results.
2. Recompute the SHA3-256 of a row's evidence file and compare to the register.
3. Walk the AIOSS chain from genesis to head `d9dcc951c9b29ad2df8733b0c6e53f98c8aa47d00177535cad948be51e8c85c9` and confirm every link.
4. Break one artifact and observe the chain fail to verify.

## Licence for teaching

Apache 2.0 terms apply to academic and teaching use. See `24_ANTICOMMONS_LICENSE`.
