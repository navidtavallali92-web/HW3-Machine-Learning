# HW3 — Regression and Classification

Two tabular datasets, three PyTorch architectures per task, model comparison, and ONNX Runtime Web deployment.

## Deploy

Upload the **contents of this project** to a GitHub repository. In **Settings → Pages**, choose **Deploy from a branch**, branch `main`, folder `/docs`. GitHub Pages will serve `docs/index.html`.

**Important:** Keep both `model.onnx` and `model.onnx.data` together in each model directory. The `.onnx.data` files contain external weights. If browser inference fails due to external-data fetching, re-export each ONNX model with embedded weights and replace both files; ONNX Runtime Web compatibility is not yet confirmed.

## Data and results

`results/` contains original training histories, comparisons, preprocessing JSON, and trained model artifacts. `figures/` contains generated plots. The classification model predicts logit for positive class malignant, converted to probability by sigmoid in JavaScript. The regression model emits MPa directly.

## Sources

UCI Concrete Compressive Strength: https://archive.ics.uci.edu/dataset/165/concrete+compressive+strength

UCI Breast Cancer Wisconsin Diagnostic: https://archive.ics.uci.edu/dataset/17/breast+cancer+wisconsin+diagnostic

## Limitations

Browser inference has not yet been verified. The test scores are based on a single random split; perfect classification scores do not establish clinical utility. Correlation heatmaps, residual plots, and a complete report still require additional analysis.
