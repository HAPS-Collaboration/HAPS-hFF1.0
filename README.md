# HAPS-hFF1.0

````markdown
# HAPS-hFF1.0

**Revisiting Unidentified Charged-Hadron Fragmentation Functions with Modern COMPASS SIDIS Multiplicities**

This repository provides the public grids, documentation, and usage examples for **HAPS-hFF1.0**, a new global QCD analysis of unidentified charged-hadron fragmentation functions (FFs).

The analysis combines single-inclusive electron--positron annihilation (SIA) data with the modern COMPASS semi-inclusive deep-inelastic scattering (SIDIS) multiplicities. The COMPASS input consists of the 2025 proton-target measurement and the revised isoscalar-target multiplicities provided in the 2026 COMPASS addendum.

The `HAPS-hFF1.0` FF replicas are provided in **LHAPDF format** for phenomenological applications.

---

## Physics scope

`HAPS-hFF1.0` determines fragmentation functions for unidentified charged hadrons,

\[
e^+e^- \to h^\pm + X,
\qquad
\ell N \to \ell h^\pm X ,
\]

using a global SIA+SIDIS QCD analysis.

The main features of the analysis are:

- global determination of unidentified charged-hadron FFs;
- inclusion of SIA data from TASSO, TPC, ALEPH, DELPHI, OPAL, and SLD;
- inclusion of the COMPASS 2025 proton-target SIDIS multiplicities;
- inclusion of the revised isoscalar-target multiplicities from the 2026 COMPASS addendum;
- NLO and NNLO extractions;
- neural-network parametrization of FFs;
- Monte Carlo replica uncertainty propagation;
- public LHAPDF grids for phenomenological use.

The modern COMPASS SIDIS input provides important charge-separated information for the light-quark and antiquark fragmentation sectors. The gluon FF remains less directly constrained in the present SIA+SIDIS-only analysis and can be further improved in future studies including hadron-collider charged-particle data.

---

## Repository contents

The repository contains, or will contain, the following material:

```text
HAPS-hFF1.0/
│
├── README.md
├── LHAPDF/
│   └── HAPS-hFF1.0/
│       ├── HAPS-hFF1.0.info
│       ├── HAPS-hFF1.0_0000.dat
│       ├── HAPS-hFF1.0_0001.dat
│       └── ...
│
├── examples/
│   ├── example_lhapdf.py
│   └── plot_haps_hff10.py
│
├── plots/
│   └── ...
│
└── docs/
    └── ...
````

The exact file structure may be updated as the public release is finalized.

---

## Installation

The grids are distributed in LHAPDF format. To use them, first make sure that LHAPDF is installed.

For example, using a conda environment:

```bash
conda install -c conda-forge lhapdf
```

or using a local LHAPDF installation:

```bash
lhapdf --version
```

Then clone this repository:

```bash
git clone https://github.com/HAPS-Collaboration/HAPS-hFF1.0.git
cd HAPS-hFF1.0
```

Copy or link the `HAPS-hFF1.0` grid directory to your LHAPDF data path. For example:

```bash
cp -r LHAPDF/HAPS-hFF1.0 $LHAPDF_DATA_PATH/
```

If `LHAPDF_DATA_PATH` is not set, you can define it manually, for example:

```bash
export LHAPDF_DATA_PATH=$HOME/local/share/LHAPDF
mkdir -p $LHAPDF_DATA_PATH
cp -r LHAPDF/HAPS-hFF1.0 $LHAPDF_DATA_PATH/
```

Check that the set is visible to LHAPDF:

```bash
lhapdf list | grep HAPS-hFF1.0
```

---

## Basic usage in Python

A simple example for reading the FF grids with LHAPDF:

```python
import lhapdf

# Load the central member or a given replica
ff = lhapdf.mkPDF("HAPS-hFF1.0", 0)

z = 0.3
Q = 5.0

# Example parton IDs:
#  1 = d, 2 = u, 3 = s, 4 = c, 5 = b, 21 = g
u_ff = ff.xfxQ(2, z, Q)
d_ff = ff.xfxQ(1, z, Q)
g_ff = ff.xfxQ(21, z, Q)

print("z D_u^{h+}(z,Q) =", u_ff)
print("z D_d^{h+}(z,Q) =", d_ff)
print("z D_g^{h+}(z,Q) =", g_ff)
```

Please check the accompanying documentation and examples for the precise grid conventions, flavor definitions, and uncertainty treatment.

---

## Perturbative orders

The analysis provides NLO and NNLO determinations.

At NNLO, the SIA coefficient functions and timelike DGLAP evolution are included at NNLO accuracy. The SIDIS coefficient functions are implemented through the available approximate NNLO corrections derived from threshold-resummed expressions.

Therefore, the NNLO result should be interpreted as a perturbative-stability extension of the SIA+modern-COMPASS-SIDIS extraction.

---

## Citation

If you use `HAPS-hFF1.0` in a publication, please cite the corresponding paper and this repository.

```bibtex
@misc{HAPShFF10,
  author       = {{HAPS Collaboration}},
  title        = {{Public grids of HAPS-hFF1.0}},
  howpublished = {\url{https://github.com/HAPS-Collaboration/HAPS-hFF1.0}},
  year         = {2026}
}
```

A paper citation will be added here once the manuscript is available on arXiv or published.

---

## Contact

For questions about the grids, usage examples, or the analysis, please contact the HAPS Collaboration.

Repository:

```text
https://github.com/HAPS-Collaboration/HAPS-hFF1.0
```

---

## License

Please check the license file of this repository before redistribution or use in external packages.

If no license file is present, contact the authors before redistributing the grids or derived material.

```
```
