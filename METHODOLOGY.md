# Methodology: Anisotropic Mitochondrial Manifold Audit (AMMA)

## 1. Data Provenance
The dataset consists of high-resolution structural coordinates retrieved from the RCSB Protein Data Bank (PDB). 
- **Inclusion Criteria:** X-Ray Diffraction or Cryo-EM structures.
- **Resolution Filter:** ≤ 2.0 Å.
- **Targeting:** Mitochondrial enzyme complexes (I, II, III, IV, and ATP Synthase).
- **Validation:** Only experimental data is used. No AI-predicted (AlphaFold) structures are included.

## 2. Geometric Feature Extraction
Protein backbones are treated as a discrete topological manifold.
- **Bond Angles (θ):** Calculated using CA(i-1)-CA(i)-CA(i+1) vectors.
- **Torsion Angles (ψ):** Derived from the C-N-CA-C dihedral matrix.
- **Logic:** The analysis focuses on Identifying Non-Invariant Geometric Constants (NIGCs).

## 3. Statistical Sieve
- **GMM Partitioning:** We utilize 4-component Gaussian Mixture Models to differentiate between stochastic noise and deterministic structural modes.
- **BIC Delta:** A Bayesian Information Criterion comparison is used to reject the single-mode (normal distribution) hypothesis.
- **Anderson-Darling Test:** Used to quantify the non-invariance of the manifold distribution.

## 4. Key Findings (Public Data)
- **Topological Information Partitioning (TIP):** Significant modes detected at 108.02° (Bond Angle) and 51.51° (Torsion Gradient).
