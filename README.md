# Deep-Learning-Enabled-Unbiased-Nanoscale-Precision-Toxicity-Prediction
one can visit the raw data and deep learning model at the link https://drive.google.com/drive/folders/1Kmw7ZN5fD2UyVsAj479g13qyK8MgGksz?usp=sharing

The repository is organized as follows:

* **`training data`**
  This directory contains all datasets collected from our previous experiments, and the images together with their manual masks were used to train the U-Net model. The folder has 4 subfolders denote 4 cell types. Each of the four cell-type subfolders (`SKM`, `IPL`, `PRL`, and `SC`) includes data folders and Jupyter notebooks: the `raw data` folder stores original images, `data` contains the prepared training and validation sets, `model weight` holds trained U-Net weights, and `result-compare thre` stores outputs used to compare deep-learning segmentation with thresholding methods. The key notebooks are `prepare data.ipynb` (prepares the training/validation datasets), `Unet.ipynb` (model training), `analysis.ipynb` (applies the trained U-Net to new experimental images and performs downstream analysis), and `compare deep learning-threshold.ipynb` (compares deep-learning and thresholding segmentation results), together providing a complete, reproducible pipeline from raw images to model training, inference, and method comparison.

* **`newest data`**
  Holds the most recent experimental images, which were reserved exclusively for evaluating U-Net’s segmentation performance. The `/training data/SKM/analysis.ipynb` notebook and also `analysis.ipynb` in other cells uses the data in `newest data` for analysis, and the resulting outputs are saved in the `newest data prediction` directory.

* **`newest data prediction`**
  This directory contains the U-Net predictions for the `newest data`.

* **`SKM (objectivity testing)`**
  Includes the raw and processed data corresponding to Figure 3 in the manuscript, demonstrating the model’s ability to deliver consistent, objective results.

* **`SKM (robustness testing)`**
  Contains the datasets used for Figure 4, designed to challenge the model under various perturbations and verify its robustness.

