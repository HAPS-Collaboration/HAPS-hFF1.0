<p align="left">
  <img src="https://img.shields.io/badge/HAPS--hFF1.0-Unidentified%20Charged--Hadron%20FF%20Set-red?style=for-the-badge" alt="HAPS-hFF1.0 — Unidentified Charged-Hadron FF Set">
</p>

# HAPS-hFF1.0

**HAPS-hFF1.0** is a set of unidentified charged-hadron fragmentation functions (FFs) developed within the **HAPS Collaboration**. The grids are distributed in **LHAPDF6** format and include next-to-leading-order (NLO) and next-to-next-to-leading-order (NNLO) determinations.

The grids accompany the publication:

> **Revisiting Unidentified Charged-Hadron Fragmentation Functions with Modern COMPASS SIDIS Multiplicities**  
> Maryam Soleymaninia, Hamzeh Khanpour, Hubert Spiesberger, Majid Azizi, Michael Klasen, and Hadi Hashamipour (HAPS Collaboration)

## Paper

- **Title:** Revisiting Unidentified Charged-Hadron Fragmentation Functions with Modern COMPASS SIDIS Multiplicities
- **Authors:** Maryam Soleymaninia, Hamzeh Khanpour, Hubert Spiesberger, Majid Azizi, Michael Klasen, and Hadi Hashamipour
- **Collaboration:** HAPS Collaboration
- **Journal:** *Physical Review D* **114**, 054013 (2026)
- **DOI:** https://doi.org/10.1103/8zzz-6xkn
- **arXiv:** https://arxiv.org/abs/2605.31325
- **INSPIRE:** https://inspirehep.net/literature/3162974
- **LHAPDF grids:** https://github.com/HAPS-Collaboration/HAPS-hFF1.0

## Physics scope

HAPS-hFF1.0 provides unidentified charged-hadron fragmentation functions extracted from a global QCD analysis combining single-inclusive electron–positron annihilation (SIA) data with modern semi-inclusive deep-inelastic-scattering (SIDIS) multiplicities from COMPASS.

The COMPASS input includes the 2025 proton-target measurements and the revised isoscalar-target multiplicities from the 2026 COMPASS addendum. The revised isoscalar measurements supersede the earlier COMPASS results used in previous global charged-hadron FF analyses.

The charge-separated COMPASS multiplicities constrain the light-quark and antiquark FFs and improve the flavor decomposition of unidentified charged-hadron production. The fits are performed at NLO and NNLO using neural-network parametrizations and Monte Carlo replicas to propagate experimental uncertainties. The comparison across perturbative orders indicates a relatively stable quark-sector determination, while the gluon FF remains less directly constrained by the SIA+SIDIS inputs.

The resulting replica ensembles are supplied in standard LHAPDF format.

## Available LHAPDF grids

**Six compressed grid archives** are available, covering positively charged hadrons (`h+`), negatively charged hadrons (`h-`), and their charge sum (`h+ + h-`) at both NLO and NNLO.

| Grid archive | Hadron final state | Order | Download |
| --- | --- | :---: | --- |
| `HAPS-hFF1.0-plus-NLO.zip` | `h+` | NLO | [ZIP](https://github.com/HAPS-Collaboration/HAPS-hFF1.0/blob/main/HAPS-hFF1.0-plus-NLO.zip) |
| `HAPS-hFF1.0-plus-NNLO.zip` | `h+` | NNLO | [ZIP](https://github.com/HAPS-Collaboration/HAPS-hFF1.0/blob/main/HAPS-hFF1.0-plus-NNLO.zip) |
| `HAPS-hFF1.0-minus-NLO.zip` | `h-` | NLO | [ZIP](https://github.com/HAPS-Collaboration/HAPS-hFF1.0/blob/main/HAPS-hFF1.0-minus-NLO.zip) |
| `HAPS-hFF1.0-minus-NNLO.zip` | `h-` | NNLO | [ZIP](https://github.com/HAPS-Collaboration/HAPS-hFF1.0/blob/main/HAPS-hFF1.0-minus-NNLO.zip) |
| `HAPS-hFF1.0-sum-NLO.zip` | `h+ + h-` | NLO | [ZIP](https://github.com/HAPS-Collaboration/HAPS-hFF1.0/blob/main/HAPS-hFF1.0-sum-NLO.zip) |
| `HAPS-hFF1.0-sum-NNLO.zip` | `h+ + h-` | NNLO | [ZIP](https://github.com/HAPS-Collaboration/HAPS-hFF1.0/blob/main/HAPS-hFF1.0-sum-NNLO.zip) |

Here, `plus` and `minus` designate the observed hadron charge, while `sum` designates the charge-summed final state. These are **unidentified charged hadrons**, not identified pion or kaon sets.

**Note:** The LHAPDF set directory and set name used inside each ZIP archive should be checked against its `.info` file. Do not assume that the ZIP filename is automatically the name accepted by `lhapdf.mkPDF`.

## Repository structure

The updated repository distributes the six compressed LHAPDF-grid archives at its root:

```text
HAPS-hFF1.0/
├── HAPS-hFF1.0-minus-NLO.zip
├── HAPS-hFF1.0-minus-NNLO.zip
├── HAPS-hFF1.0-plus-NLO.zip
├── HAPS-hFF1.0-plus-NNLO.zip
├── HAPS-hFF1.0-sum-NLO.zip
├── HAPS-hFF1.0-sum-NNLO.zip
└── README.md
```

Each ZIP archive is a downloadable package for a specified hadron-charge combination and perturbative order. **The ZIP archives must be extracted before their LHAPDF sets can be installed.**

## Download and extraction

For an individual set, select its **ZIP** link in the table above and choose **Download raw file** on GitHub. You do not need to clone the entire repository to obtain a single archive.

Alternatively, clone the repository:

```bash
git clone https://github.com/HAPS-Collaboration/HAPS-hFF1.0.git
cd HAPS-hFF1.0
```

Extract an archive, for example the positive-hadron NLO grids:

```bash
unzip HAPS-hFF1.0-plus-NLO.zip -d extracted-plus-NLO
```

Inspect its contents to identify the actual LHAPDF set directory:

```bash
find extracted-plus-NLO -type f -name '*.info'
```

## Install and use with LHAPDF

1. Install **LHAPDF6** and ensure `lhapdf-config` is available.
2. Extract the desired ZIP file.
3. Find the directory containing its `.info` file and companion `.dat` replica files.
4. Copy that **entire directory** (not just the `.info` file) into the LHAPDF data directory shown by:

```bash
lhapdf-config --datadir
```

For example, after identifying the extracted set directory, install it using:

```bash
cp -r /path/to/extracted/LHAPDF_SET_DIRECTORY "$(lhapdf-config --datadir)/"
```

Replace `/path/to/extracted/LHAPDF_SET_DIRECTORY` with the **actual directory** located inside the archive. The directory must contain the matching `<set-name>.info` file and its member `.dat` files.

Check the installed set with:

```bash
lhapdf show LHAPDF_SET_NAME
```

Replace `LHAPDF_SET_NAME` with the set name given by the installed `.info` filename (without the `.info` extension). In Python, it can then be loaded as:

```python
import lhapdf

ff = lhapdf.mkPDF("LHAPDF_SET_NAME", 0)
z, Q = 0.2, 10.0
print(ff.xfxQ(2, z, Q))  # z * D_u^h(z, Q) for the selected hadron set
```

**Important:** Use an NLO or NNLO FF set together with a consistently matched perturbative-order calculation, and consult the grid metadata for member numbering, supported flavors, and kinematic coverage.

## Citation

If you use HAPS-hFF1.0 in a publication, please cite:

> M. Soleymaninia *et al.* (HAPS Collaboration), *Revisiting unidentified charged-hadron fragmentation functions with modern COMPASS SIDIS multiplicities*, **Phys. Rev. D 114**, 054013 (2026). https://doi.org/10.1103/8zzz-6xkn

```bibtex
@article{Soleymaninia:2026xjq,
  author        = {Soleymaninia, Maryam and Khanpour, Hamzeh and
                   Spiesberger, Hubert and Azizi, Majid and
                   Klasen, Michael and Hashamipour, Hadi},
  collaboration = {HAPS},
  title         = {Revisiting Unidentified Charged-Hadron Fragmentation
                   Functions with Modern COMPASS SIDIS Multiplicities},
  journal       = {Phys. Rev. D},
  volume        = {114},
  pages         = {054013},
  year          = {2026},
  doi           = {10.1103/8zzz-6xkn},
  eprint        = {2605.31325},
  archivePrefix = {arXiv},
  primaryClass  = {hep-ph}
}
```

## Related HAPS fragmentation-function grids

- **Charged-pion FFs (HAPS-PiFF1.0):** https://github.com/HAPS-Collaboration/HAPS-PiFF1.0
- **Charged-kaon FFs (HAPS-KaFF1.0):** https://github.com/HAPS-Collaboration/HAPS-KaFF1.0

## Related resources

- **HAPS Collaboration:** https://github.com/HAPS-Collaboration
- **arXiv:** https://arxiv.org/abs/2605.31325
- **INSPIRE:** https://inspirehep.net/literature/3162974
- **Published article:** https://doi.org/10.1103/8zzz-6xkn
