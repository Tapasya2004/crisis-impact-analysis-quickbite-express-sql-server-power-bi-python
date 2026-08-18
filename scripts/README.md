# Scripts

This folder is reserved for reusable Python source files extracted from the analytical notebook.

The current project artifact is the Jupyter notebook in `notebooks/`. The notebook should remain the source of truth until the workflow is separated into production-style modules.

Suggested future modules:

```text
scripts/
├── data_loader.py
├── feature_engineering.py
├── customer_segmentation.py
├── recovery_scoring.py
└── run_analysis.py
```
