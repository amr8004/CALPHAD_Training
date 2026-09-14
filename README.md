# pycalphad + Scheil Demo Notebook

A self-contained walkthrough of core CALPHAD workflows using [pycalphad](https://pycalphad.org/) and the [`scheil`](https://github.com/PhasesResearchLab/scheil) package, built around a Fe-Cr-Ni thermodynamic database. Useful as a starting point for anyone learning CALPHAD-style equilibrium and solidification calculations in Python.

## What's inside

The notebook (`training.ipynb`) steps through five worked examples on the `Cr-Fe-Ni_miettinen1999.tdb` database:

1. **Gibbs energy curve** — molar Gibbs energy of the LIQUID phase vs. temperature at fixed composition
2. **Binary Fe-Cr phase diagram** — isobaric phase diagram for the Fe-Cr subsystem
3. **Ternary Fe-Cr-Ni phase diagram** — isothermal section at 1300 K
4. **Single equilibrium calculation** — one-point equilibrium with a full breakdown of the returned `xarray` Dataset
5. **Scheil solidification** — single-composition Scheil simulation with a temperature vs. liquid-fraction plot

## Requirements

- Python 3.11+
- [`pycalphad`](https://pycalphad.org/)
- [`scheil`](https://github.com/PhasesResearchLab/scheil)
- `numpy`, `matplotlib`, `xarray`

## Getting started (GitHub Codespaces)
 
This repo is set up to run entirely in [GitHub Codespaces](https://github.com/features/codespaces) — no local Python setup required.
 
1. Click **Code → Codespaces → Create codespace on main** (or use the badge below).
2. Wait for the container to build; dependencies install automatically.
3. Open `training.ipynb` and run the cells in order.
[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://github.com/codespaces/new?repo=<amr8004>/<CALPHAD_Training>)
 
### Running locally instead
 
If you'd rather not use Codespaces:
 
```bash
git clone <this-repo-url>
cd <this-repo>
pip install pycalphad scheil matplotlib numpy xarray
jupyter notebook training.ipynb
```
 
## Requirements
 
Handled automatically inside the Codespace (see `.devcontainer/`); if running locally, install manually:
 
- Python 3.11+
- [`pycalphad`](https://pycalphad.org/)
- [`scheil`](https://github.com/PhasesResearchLab/scheil)
- `numpy`, `matplotlib`, `xarray`
Make sure `Cr-Fe-Ni_miettinen1999.tdb` is in the expected data path referenced at the top of the notebook before running the cells.

## Notes

- Output attribute names for Scheil results can vary slightly across `scheil` package versions; the notebook checks for expected attributes before plotting so it stays robust across environments.
- Each section is independent enough to copy into your own scripts as a starting template for equilibrium or solidification calculations on other systems/databases.

## License

Add a license of your choice (e.g. MIT) here.
