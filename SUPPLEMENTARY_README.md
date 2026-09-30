# WaterPath-MTLNet Supplementary Reproducibility Pack

This package was generated directly from the uploaded notebook
`Waterpathogen_Q1_Advanced_(3).ipynb`.

Source notebook SHA-256:
`5bcb88939010b3b33c23be68afb30e8e0bd6db98d034d3b43d2ca38e88a3b1cc`

## Files

- `config.json`: core notebook configuration.
- `run_config.yaml`: compact human-readable run configuration.
- `dataset_spec.json`: COCO split structure, class list, audit counts, and mask-construction rules.
- `preprocessing_augmentation.json`: exact training and evaluation transformations.
- `model_spec.json`: ConvNeXt V2 encoder, FPN localization branch, and ROI-gated classifier specification.
- `training_protocol.json`: class/pixel weighting, losses, optimizer, scheduler, mixed precision, early stopping, and checkpoint logic.
- `evaluation_protocol.json`: classification, localization, bootstrap, calibration, explainability, PCA, and latency settings.
- `reproducibility.json`: deterministic settings, RNG-state handling, loader settings, figure export settings, and source hash.
- `ablation_protocol.csv`: controlled ablation configurations defined in the notebook.
- `requirements.txt`: packages explicitly installed/imported by the notebook without inventing exact runtime versions.
- `environment.yml`: portable environment template.
- `supplementary_manifest.json`: SHA-256 and size for every file in this package.

## Dataset summary recorded in the notebook

- Train: 1,055 images, 6,430 annotations.
- Validation: 301 images, 1,668 annotations.
- Test: 151 images, 924 annotations.
- Classes: Astrovirus, Cryptosporidium, Giardia, Norovirus, Rotavirus.
- Duplicate filenames across train/validation/test: 0.
- Missing files reported by the audit: 0.
- Only five training annotations use bounding-box fallback; all validation and test annotations use polygon/RLE geometry.

## Reproducibility note

The notebook records Python as `3.x` and installs minimum package constraints for `timm` and
`albumentations`, but it does not preserve a complete exact Colab package freeze. For this reason,
the supplementary package does not invent exact version numbers. If an exact software freeze is
required for submission, run `pip freeze > requirements-lock.txt` in the same Colab runtime used
for the final experiment.

## Recommended submission use

For a journal supplementary archive, include this package together with the final executed notebook,
the exported numerical CSV tables, and the validation-selected checkpoint if journal storage limits
permit. Large per-epoch checkpoints are normally better deposited in an external research repository
and referenced by DOI or permanent URL.
