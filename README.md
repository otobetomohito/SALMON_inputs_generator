# SALMON Input Generator

Single-file HTML app for preparing SALMON input configurations.

## Features

- SALMON namelist preview and download
- JSON export and import
- Structure viewer with atoms, bonds, and periodic cell edges
- Validation before export
- Testsuite-based templates for GS, RT-TDDFT, Maxwell-TDDFT, and multiscale setups

## Usage

Open `salmon_input_generator.html` in a web browser.

## Notes

- This repository is client-side only. No backend is required.
- The app currently keeps SALMON namelist generation and uses JSON-style canonical state internally.
- The structure viewer uses `3Dmol.js` from a public CDN.
