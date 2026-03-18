# SALMON Input Generator

Single-file HTML app for preparing SALMON input configurations.

## Features

- SALMON namelist preview and download
- JSON export and import with canonical-state metadata and schema versioning
- Validation before namelist or JSON export
- Upload and validate existing SALMON input files before loading them into the form
- Structure viewer with atoms, bonds, and periodic cell edges
- Testsuite-based templates for GS, RT-TDDFT, Maxwell-TDDFT, and multiscale setups
- Support for optional second-pulse RT fields and polarization vectors

## Usage

Open `salmon_input_generator.html` in a web browser.

Typical workflow:

1. Start from a testsuite-based template or import a CIF / JSON / SALMON input file
2. Inspect the generated structure in the viewer
3. Check the Validation Summary for errors and warnings
4. Export SALMON namelist or JSON only after validation passes

## Notes

- This repository is client-side only. No backend is required.
- The app keeps SALMON namelist generation and uses a JSON-style canonical state internally.
- Exported JSON includes `metadata.schema_version` and `metadata.template_name` for future compatibility.
- Imported JSON currently accepts schema version `1.x` and requires `system.atomic_coordinate_mode`.
- The structure viewer uses `3Dmol.js` from a public CDN.
- Uploaded SALMON input parsing is intentionally partial: supported keywords are validated, unsupported keywords are reported as warnings.
