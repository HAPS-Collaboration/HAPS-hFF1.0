**HAPS-hFF1.0**

**Revisiting Unidentified Charged-Hadron Fragmentation Functions with Modern COMPASS SIDIS Multiplicities**

<p align="left">
  <img src="https://img.shields.io/badge/HAPS--hFF1.0-Unidentified%20Charged--Hadron%20FF%20Set-red?style=for-the-badge" alt="HAPS-hFF1.0">
</p>

# HAPS-hFF1.0

**HAPS-hFF1.0** is an unidentified charged-hadron fragmentation-function set developed within the **HAPS Collaboration**.

The grids accompany the analysis:

> **Revisiting Unidentified Charged-Hadron Fragmentation Functions with Modern COMPASS SIDIS Multiplicities**
> Maryam Soleymaninia, Hamzeh Khanpour, Hubert Spiesberger, Majid Azizi, Michael Klasen, and Hadi Hashamipour

## Paper

* **Title:** Revisiting Unidentified Charged-Hadron Fragmentation Functions with Modern COMPASS SIDIS Multiplicities
* **Authors:** Maryam Soleymaninia, Hamzeh Khanpour, Hubert Spiesberger, Majid Azizi, Michael Klasen, and Hadi Hashamipour
* **Collaboration:** HAPS Collaboration
* **arXiv:** https://arxiv.org/abs/2605.31325
* **INSPIRE:** https://inspirehep.net/literature/3162974
* **DOI:**
* **LHAPDF grids:** https://github.com/HAPS-Collaboration/HAPS-hFF1.0

## Physics scope

HAPS-hFF1.0 provides unidentified charged-hadron fragmentation functions extracted from a global QCD analysis combining single-inclusive electron-positron annihilation data with modern semi-inclusive deep-inelastic-scattering multiplicities from COMPASS.

The COMPASS input includes the 2025 proton-target multiplicities and the revised isoscalar-target multiplicities provided in the 2026 COMPASS addendum. The revised isoscalar measurements supersede the earlier COMPASS results used in previous global charged-hadron fragmentation-function analyses.

The charge-separated COMPASS multiplicities provide important constraints on the light-quark and antiquark fragmentation functions and improve the flavor decomposition of unidentified charged-hadron production.

The extraction is performed at next-to-leading order and next-to-next-to-leading order. The comparison between the two perturbative orders indicates a stable quark-sector determination, while the gluon fragmentation function remains less directly constrained in the present SIA+SIDIS analysis.

The resulting Monte Carlo replica sets are provided in standard LHAPDF format.

## Available LHAPDF grids

This repository contains two unidentified charged-hadron fragmentation-function sets:

| Grid directory     |           Hadron final state | Perturbative order |
| ------------------ | ---------------------------: | -----------------: |
| `HAPS-hFF1.0-NLO`  | Unidentified charged hadrons |                NLO |
| `HAPS-hFF1.0-NNLO` | Unidentified charged hadrons |               NNLO |

## Repository structure

```text
HAPS-hFF1.0/
├── HAPS-hFF1.0-NLO/
├── HAPS-hFF1.0-NNLO/
└── README.md
```

Each grid directory contains an LHAPDF `.info` file and the corresponding Monte Carlo replica files.

## Related identified-hadron grids

The corresponding HAPS charged-pion and charged-kaon fragmentation-function grids are available at:

* **HAPS-PiFF1.0:** https://github.com/HAPS-Collaboration/HAPS-PiFF1.0
* **HAPS-KaFF1.0:** https://github.com/HAPS-Collaboration/HAPS-KaFF1.0

## Citation

When using these grids, please cite:

```bibtex
%\cite{Soleymaninia:2026xjq}
\bibitem{Soleymaninia:2026xjq}
M.~Soleymaninia \textit{et al.} [HAPS],
%``Revisiting Unidentified Charged-Hadron Fragmentation Functions with Modern COMPASS SIDIS Multiplicities,''
[arXiv:2605.31325 [hep-ph]].
%1 citations counted in INSPIRE as of 24 Jun 2026
```

## Related resources

* HAPS Collaboration: https://github.com/HAPS-Collaboration
* HAPS-PiFF1.0: https://github.com/HAPS-Collaboration/HAPS-PiFF1.0
* HAPS-KaFF1.0: https://github.com/HAPS-Collaboration/HAPS-KaFF1.0
* arXiv: https://arxiv.org/abs/2605.31325
* INSPIRE: https://inspirehep.net/literature/3162974

