# CORE BIOIMAGE IO PYTHON

![license](https://img.shields.io/badge/license-MIT-blue) ![offline-first](https://img.shields.io/badge/offline--first-air--gap-green) ![audit](https://img.shields.io/badge/audit-SHA3--256-orange) ![category](https://img.shields.io/badge/category-scientific_lab-lightgrey)

> Anticloud-hardened packaging of the upstream project `CORE_BIOIMAGE_IO_PYTHON` in category **SCIENTIFIC LAB**. Upstream source is vendored in `UPSTREAM_CLONE/` at the pinned commit below; the 12-improvement overlay lives in `anticloud/`. Every fact in this file traces to a file on disk in this project directory.

**Category:** SCIENTIFIC LAB · **Upstream:** https://github.com/bioimage-io/core-bioimage-io-python · **Upstream pin:** `31703b23e9d666a94bedab248411d95348a18ab3` · **Vendor:** Anticloud FZ LLE

---

## What This Project Does

![License](https://img.shields.io/github/license/bioimage-io/core-bioimage-io-python.svg)
[![PyPI](https://img.shields.io/pypi/v/bioimageio-core.svg?style=popout)](https://pypi.org/project/bioimageio.core/)
[![conda-version](https://anaconda.org/conda-forge/bioimageio.core/badges/version.svg)](https://anaconda.org/conda-forge/bioimageio.core/)
[![downloads](https://static.pepy.tech/badge/bioimageio.core)](https://pepy.tech/project/bioimageio.core)
[![conda-forge downloads](https://img.shields.io/conda/dn/conda-forge/bioimageio.core.svg?label=conda-forge)](https://anaconda.org/conda-forge/bioimageio.core/)
![code style](https://img.shields.io/badge/code%20style-black-000000.svg)
[![coverage](https://bioimage-io.github.io/core-bioimage-io-python/coverage/coverage-badge.svg)](https://bioimage-io.github.io/core-bioimage-io-python/coverage/index.html)

# bioimageio.core

`bioimageio.core` is a python package that implements prediction with bioimage.io models
including standardized pre- and postprocessing operations.
Such models are represented as [bioimageio.spec](https://bioimage-io.github.io/spec-bioimage-io) resource descriptions.

In addition bioimageio.core provides functionality to convert model weight formats
and compute selected dataset statistics used for preprocessing.

## Documentation

[Here you find the bioimageio.core documentation.](https://bioimage-io.github.io/core-bioimage-io-python)

#### Examples

Notebooks that save and load resource descriptions and validate their format (using <a href="https://bioimage-io.github.io/spec-bioimage-io/">bioimageio.spec</a>, a dependency of bioimageio.core)
<ul>
<li><a href="https://github.com/bioimage-io/spec-bioimage-io/blob/main/example/load_model_and_create_your_own.ipynb">load_model_and_create_your_own.ipynb</a> <a target="_blank" href="https://colab.research.google.com/github/bioimage-io/spec-bioimage-io/blob/main/example/load_model_and_create_your_own.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a></li>
<li><a href="https://github.com/bioimage-io/spec-bioimage-io/blob/main/example/dataset_creation.ipynb">dataset_creation.ipynb</a> <a target="_blank" href="https://colab.research.google.com/github/bioimage-io/spec-bioimage-io/blob/main/example/dataset_creation.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a></li>
</ul>

Use the described resources in Python with <a href="https://bioimage-io.github.io/core-bioimage-io-python/">bioimageio.core</a>
<ul>
<li><a href="https://github.com/bioimage-io/core-bioimage-io-python/blob/main/example/model_usage.ipynb">model_usage.ipynb</a><a target="_blank" href="https://colab.research.google.com/github/bioimage-io/core-bioimage-io-python/blob/main/example/model_usage.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a></li>
</ul>

#### Presentations

- [Create a model from scratch](https://bioimage-io.github.io/core-bioimage-io-python/presentations/create_ambitious_sloth.slides.html) ([source](https://github.com/bioimage-io/core-bioimage-io-python/tree/main/presentations))

## Set up Development Environment

To set up a development environment run the following commands:

```console
conda create -n core python=$(grep -E '^requires-python' pyproject.toml | grep -oE '[0-9]+\.[0-9]+')
conda activate core
pip install -e .[dev,partners]
```

### Joint development of bioimageio.spec and bioimageio.core

Assuming [spec-bioimage-io](https://github.com/bioimage-io/spec-bioimage-io) is sourced to the parent folder
a joint development environment can be created with the following commands:

```console
conda create -n core python=$(grep -E '^requires-python' pyproject.toml | grep -oE '[0-9]+\.[0-9]+')
conda activate core
pip install -e .[dev,partners] -e ../spec-bioimage-io[dev]
```

## Logging level

`bioimageio.spec` and `bioimageio.core` use [loguru](https://github.com/Delgan/loguru) for logging, hence the logging level
may be controlled with the `LOGURU_LEVEL` environment variable.
The `bioimageio` CLI has logging enabled by default.
To activate logging when using bioimageio.spec/bioimageio.core as a library, add

```python
from loguru import logger

logger.enable("bioimageio")
```

## Changelog

See [changelog.md](changelog.md)

*Quoted from the upstream `README.md` file in `UPSTREAM_CLONE/`.*
Project-specific facts detected in this directory:

- Ecosystem: **Python** (manifests: pyproject.toml; scanned in UPSTREAM_CLONE)
- Top-level source layout: `conda-recipe/`, `example/`, `presentations/`, `scripts/`, `src/`, `tests/`
- Snapshot size: **76 files**, **13123 lines of code** (measured; see Benchmarks)
- Primary languages: `.py` (57), `.yaml` (6), `.yml` (3), `(none)` (2), `.md` (2), `.html` (1)
- Upstream commit pinned for this packaging: `31703b23e9d666a94bedab248411d95348a18ab3`

---

## Installation

No installation section was found in the upstream readme, so the commands below are generated from the manifests detected in this project directory.

```sh
python -m venv .venv && source .venv/bin/activate   # Windows: .venv\Scripts\activate
pip install -e .                                     # or: pip install -r requirements.txt
```

Overlay install (this project):

```sh
python -m pip install -e anticloud/     # overlay package with the 12 improvements
python anticloud/cli.py --help          # 13 subcommands, JSON stdout
```

---

## Usage

Notebooks that save and load resource descriptions and validate their format (using <a href="https://bioimage-io.github.io/spec-bioimage-io/">bioimageio.spec</a>, a dependency of bioimageio.core)
<ul>
<li><a href="https://github.com/bioimage-io/spec-bioimage-io/blob/main/example/load_model_and_create_your_own.ipynb">load_model_and_create_your_own.ipynb</a> <a target="_blank" href="https://colab.research.google.com/github/bioimage-io/spec-bioimage-io/blob/main/example/load_model_and_create_your_own.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a></li>
<li><a href="https://github.com/bioimage-io/spec-bioimage-io/blob/main/example/dataset_creation.ipynb">dataset_creation.ipynb</a> <a target="_blank" href="https://colab.research.google.com/github/bioimage-io/spec-bioimage-io/blob/main/example/dataset_creation.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a></li>
</ul>

Use the described resources in Python with <a href="https://bioimage-io.github.io/core-bioimage-io-python/">bioimageio.core</a>
<ul>
<li><a href="https://github.com/bioimage-io/core-bioimage-io-python/blob/main/example/model_usage.ipynb">model_usage.ipynb</a><a target="_blank" href="https://colab.research.google.com/github/bioimage-io/core-bioimage-io-python/blob/main/example/model_usage.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a></li>
</ul>

*Section quoted from the upstream readme.*
Anticloud overlay CLI (available in every project):

```sh
python anticloud/cli.py --help     # 13 subcommands, JSON stdout
python anticloud/cli.py checks     # run the 16-check suite
```

---

## API

[Here you find the bioimageio.core documentation.](https://bioimage-io.github.io/core-bioimage-io-python)

*Section quoted from the upstream readme.*
---

## Dependencies

| Metric | Value |
|--------|-------|
| Ecosystem | Python |
| Manifests detected | pyproject.toml |
| Files in snapshot | 76 |
| Lines of code | 13123 |
| Dependency references | 12 |
| Dependencies by ecosystem | pypi: 12 |
| Upstream license | MIT |
| Overlay license | Anticommons 0.1.0 |

Top dependency references recorded in the benchmark snapshot:

| Ecosystem | Name | Version | Source file |
|-----------|------|---------|-------------|
| pypi | bioimageio.spec | ==0.5.12.0 | pyproject.toml |
| pypi | imagecodecs | - | pyproject.toml |
| pypi | imageio | >=2.10 | pyproject.toml |
| pypi | loguru | - | pyproject.toml |
| pypi | numpy | - | pyproject.toml |
| pypi | pydantic-settings | >=2.5 | pyproject.toml |
| pypi | pydantic | >=2.7.0 | pyproject.toml |
| pypi | ruyaml | - | pyproject.toml |
| pypi | scipy | - | pyproject.toml |
| pypi | tqdm | - | pyproject.toml |
| pypi | typing-extensions | - | pyproject.toml |
| pypi | xarray | >=2023.01 | pyproject.toml |

Pinned lockfile: `anticloud/requirements.lock` (hash-pinned, PEP 508). SBOM: `sbom.cdx.json` (CycloneDX 1.5, pinned to the upstream SHA).

---

## Configuration

To set up a development environment run the following commands:

```console
conda create -n core python=$(grep -E '^requires-python' pyproject.toml | grep -oE '[0-9]+\.[0-9]+')
conda activate core
pip install -e .[dev,partners]
```

*Section quoted from the upstream readme.*
Overlay configuration (Anticloud):

- `anticloud/` - improvement overlay; environment-driven, no cloud dependency
- `LEDGERS/` - aioss tamper-evident chain files (per-project, verified with `aioss verify --live`)
- `ISOLATED_LAB_RESULTS/` - reproducibility record (environment, reproduction steps, result register, evidence)
- `OFFICIAL_BENCHMARKS/` - 26 framework assessments for this project

---

## Contributing

Upstream contributions: fork the `CORE_BIOIMAGE_IO_PYTHON` project, create a feature branch, and open a pull request against upstream. Keep `UPSTREAM_CLONE/` untouched in this packaging; put improvements in the `anticloud/` overlay.

Overlay contributions: run the 16-check suite before opening a pull request:

```sh
python anticloud/bench/runner.py --cwd anticloud
```

---

## License

**Upstream license: MIT** (evidence: `LICENSE` in the upstream snapshot).

License file excerpt:

```text
MIT License

Copyright (c) 2020 BioImage.IO

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
```

### Anticommons 0.1.0 overlay

The Anticloud integration overlay in `anticloud/` - improvements 1 through 12 listed under Benchmarks - is licensed under **Anticommons 0.1.0**. Upstream code remains under its original MIT terms. See `ANTICOMMONS_LICENSE.md` in this directory for the overlay terms and contact.

SPDX: `MIT` (upstream) + Anticommons 0.1.0 (overlay, dual).

---

## Upstream

- **Project:** `CORE_BIOIMAGE_IO_PYTHON` (category: SCIENTIFIC LAB)
- **Upstream URL:** https://github.com/bioimage-io/core-bioimage-io-python
- **Pinned commit (SHA):** `31703b23e9d666a94bedab248411d95348a18ab3`
- **Branch:** main
- **Pin provenance:** resolved during the second documentation pass. The parent-project stamp is explicitly rejected for this project.
- **Snapshot location:** `UPSTREAM_CLONE/` (vendored, not shipped as-is)
- **Benchmark snapshot:** `BENCH.json`

---

## Benchmarks

Measured by the Anticloud assurance suite. Every value below is read from this
project's `BENCH.json`, produced by a real run — the SHA3-256 of that file is
`3ca177018978949cdb3358de58c204181ba75ef160ddeac706286dd0cc7ce292`.

| Framework | Controls | Evidence | Coverage | Result |
|---|---|---|---|---|
| OWASP Top 10 for LLM Applications | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| OWASP Top 10 (2021) | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| SOC 2 Type II readiness | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| NIST AI Risk Management Framework | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| NIST SP 800-53 Rev. 5 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| NIST Cybersecurity Framework 2.0 | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| FedRAMP Rev. 5 | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| PCI DSS v4.0.1 | 11 controls mapped | 11 with evidence | 100.0% | PASS |
| ISO/IEC 27001:2022 | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| MITRE ATT&CK v16 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| ML Technology Readiness Level | TRL 8 | 8/8 criteria | | PASS |

**Overall: 16/16 checks passing.**

See `ISOLATED_LAB_RESULTS/03_Result_Register.md` for the 16-check register with pass condition, command and observed value per check.

Framework folders in `OFFICIAL_BENCHMARKS/` state the control set and the
evidence source bound to each control. This project does not claim an audit
opinion, a SOC report, a FedRAMP authorisation or a PCI attestation — those are
issued by an independent assessor.



## Archives and Permanent Records

| Platform | Identifier | Volume |
|---|---|---|
| Harvard Dataverse | DOI 10.7910/DVN/YMJKOG | 145 citable datasets |
| AIOSS verification kit | DOI 10.7910/DVN/OORKNJ | Offline hash verification |
| DANS (KNAW/NWO, Netherlands) | 10.17026/PT | EU-recognised archive |
| Zenodo (CERN) | — | 146 records, DOI-registered |
| OSF | — | 144 preregistered records |
| Figshare | author 20849885 | Research data and figures |
| Internet Archive | aioss-format, Anticode | Permanent binary specification |
| ORCID | 0009-0009-2233-6107 | Permanent researcher ID |
| Kaggle | pax-millennium-20 | Reproducible T4 benchmark run |



## Press and Independent Publication

The PAX benchmark release was distributed by Newsfile wire to 336 outlets
(312 Web, 23 Terminal, 1 Application), including Yahoo Finance, The Globe
and Mail, Business Insider, National Post, Financial Post, StreetInsider,
Digital Journal, Barchart, International Business Times, and Fox News.
Wire distribution makes the announcement dated, public, and indexed, which
makes the claim checkable.

