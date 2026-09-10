# SOA65: condition-aware SOA verification

Reproducibility materials for curve–condition binding and deterministic query verification in MOSFET safe operating area (SOA) datasheets.

## Download

[Download the complete reader package](SOA65_Public_Package.zip?raw=1) (approximately 13.0 MB).

Extract the archive to obtain the `Public_Package/` directory. Its `README.md` explains the data, implementation, experiment settings and result files.

## Reproduce the results

Python 3.12 is the recorded runtime:

```sh
cd Public_Package
python3.12 -m pip install -r requirements-replay.txt
python3.12 reproduce.py
```

After installing NumPy, the replay runs offline without API calls. It reparses 884 saved final model answers and checks 33 CSV exports, including 155,190 query-policy decisions.

To regenerate the five result tables and three quantitative main figures:

```sh
python3.12 -m pip install -r requirements-figures.txt
python3.12 paper/rebuild.py
```

## Contents

- Core implementation, experiment settings and prompts.
- Reference annotations for 65 documents and 116 analysis snapshots.
- Saved final model outputs, query decisions, checking records and aggregate tables.
- Manuscript table and quantitative-figure scripts.
- Download links for all 65 manufacturer datasheets.

Manufacturer PDFs and rendered input images are not included. Reader-facing documentation is English; original experimental evidence retains its recorded language.

## License

Original software: [MIT](LICENSE). Original annotations: CC BY 4.0, with the legal text and attribution details included in the archive. Manufacturer excerpts and other third-party material retain their respective rights.
