# Command Line Interface — CORE_BIOIMAGE_IO_PYTHON

**Upstream:** https://github.com/bioimage-io/core-bioimage-io-python

## Anticloud CLI

```bash
# Install
pip install anticloud-core-bioimage-io-python

# Run offline with PAX inference
anticloud-core-bioimage-io-python --offline --pax-local

# Run with AIOSS logging
anticloud-core-bioimage-io-python --aioss-log ./ledger.jsonl

# Single binary (after build)
./core_bioimage_io_python --config config.yaml
```

## Options

| Flag | Description |
| --- | --- |
| `--offline` | Disable all network calls |
| `--pax-local` | Use local PAX inference at 127.0.0.1:11434 |
| `--aioss-log PATH` | Write AIOSS audit chain to PATH |
| `--encrypt` | Enable AES-256 at rest for output files |
| `--gpu` | Force GPU inference |
| `--cpu` | Force CPU inference |
| `--config PATH` | Load configuration from YAML file |
