# Laser-Driven FMR Probed by XUV T-MOKE

Side project to draft a laser-driven ferromagnetic resonance (FMR) experiment with the
[udkm1Dsim](https://github.com/dschick/udkm1Dsim) toolbox, without touching its source.

A Ta 2 nm / Py 20 nm / Si film is magnetized in-plane and horizontally, i.e. in the scattering
plane. The external field is applied in the scattering plane at 30° from the surface. The pump
demagnetizes the Py, which tilts the equilibrium and drives a precession, whose vertical
component is probed by T-MOKE of a pi-polarized XUV probe at the Fe M2,3 edges.

- `laser_fmr_tmoke.ipynb`: static T-MOKE map (energy, angle), 2TM excitation, LLG precession with
  the Smit-Beljers frequency, transient T-MOKE by `Elzo`, and the symmetry of the field reversal.
- `Fe_XUV.cf`, `Fe_XUV.mf`: charge and magnetic form factors of Fe at the M2,3 edges
  (Willems et al., PRL 122, 217202 (2019)), copied from the udkm1Dsim examples.

## Setup

udkm1Dsim and mbistyles are installed in editable mode from the neighboring checkouts
`../udkm1Dsim` and `../mbistyles`.

```bash
uv sync
uv run --with jupyterlab jupyter lab  # or pick .venv as kernel in VS Code
```
