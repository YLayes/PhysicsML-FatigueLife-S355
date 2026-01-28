
***Hybrid physics–machine learning approach combining Gaussian process regression and Sines‑style invariants for multiaxial fatigue life prediction of S355 steel***

***Overview***
This repository contains the data, figures, and code supporting the manuscript *“Hybrid physics–machine learning approach combining Gaussian process regression and Sines‑style invariants for multiaxial fatigue life prediction of S355 steel.”*  
The project integrates classical fatigue invariants with Gaussian Process Regression (GPR) to improve predictive accuracy and quantify uncertainty. Hybrid residual, feature, and stacked strategies are benchmarked against physics‑only and ML‑only baselines.

***Dataset***
- **Material:** S355 structural steel fatigue dataset.  
- **Format:** Excel file (`FatigueDataS355.xlsx`) with experimental fatigue lives (Nexp), axial and shear stress components (Sm, Tm, Sa, Ta).  
- **Content:**  
  - 133 specimens after curation (removal of runouts, duplicates, outliers).  
  - Stress descriptors and fatigue life cycles in log10(Nf) space.  
- **Source:** Adapted from Karolczuk & Kluger (2019), with preprocessing and feature engineering applied.

***Methodology***
1. **Physics baselines:**  
   - Sines–Basquin invariant model.  
   - Fatemi–Socie critical plane criterion.  
2. **Machine learning baseline:**  
   - Gaussian Process Regression (GPR).  
3. **Hybrid strategies:**  
   - **Hybrid‑Residual:** GPR learns systematic residuals relative to Sines baseline.  
   - **Hybrid‑Feature:** Physics‑enriched input vectors (Sines score + stress features).  
   - **Hybrid‑Stacked:** Convex stacking of physics and GPR predictions.  
4. **Outputs:** Fatigue life predictions in log10(Nf) with calibrated 95% prediction intervals.

***Usage***
- Clone the repository:  
  ```bash
  git clone https://github.com/YLayers/PhysicsML-FatigueLife-S355.git
  cd PhysicsML-FatigueLife-S355


## Citation
If you use this dataset or code, please cite:  

> Youcef Layes, Zoubeir Tourki. *Physics‑Informed Machine Learning for Multiaxial Fatigue Life Prediction of S355 Steel.* Results in Engineering, Elsevier, 2026. (In review)

BibTeX (preprint/in review):
```bibtex
@article{Layes2026PhysicsMLFatigue,
  author    = {Youcef Layes and Zoubeir Tourki},
  title     = {Physics-Informed Machine Learning for Multiaxial Fatigue Life Prediction of S355 Steel},
  journal   = {Results in Engineering},
  year      = {2026},
  note      = {In review}
}
```

## License
- **Code:** Released under the MIT License — free to use, modify, and distribute with attribution.  
- **Data & Figures:** Released under CC BY 4.0 — free to share and adapt with proper citation.  

