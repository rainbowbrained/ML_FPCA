# Functional PCA for Dimensionality Reduction (Machine Learning 2025 Course)

Functional PCA for dimensionality reduction. Skoltech group project, ML 2025

 ![hands](https://github.com/user-attachments/assets/5ad5a069-0a99-43d9-a2ff-80c8a2478bac)

Image reconstruction for HaGRID dataset for different number of components and resolutions

PCA is the simplest linear method for dimensionaliy reduction. It learns the set of basis vectors that fits the data in the most parsimonius way. Sometimes data can be analyzed not in terms of a set of distinct features (like usual tabular data), but rather as a functions, evaluated at some grid (time series, images, video). Changing the resolution is simply the change of grid at which the functions are evaluated. For functional data there exist an extesion of PCA called Functional PCA (FPCA). In this project our goal was to explore the FPCA approach to dimensionality reductoin, its advantages and disadvantages over the classical PCA, its limitations and ways to overcome them.

# Research steps

1. We conducted a literature review on FPCA, including papers devoted to the basic idea of ​​the method and papers devoted to the problem in a high-dimensional space and with sparse data. The files reports/early_report.pdf and reports/final_report.pdf correspond to this part of the study

2. We applied FPCA to the evaluation of a polynomial function on a finite grid (with added noise). The goal was to predict the order of the polynomial. We were able to estimate the influence of noise, the number of components, and the influence of being in the neighborhood of zero. The file notebooks/FPCA_Toy.ipynb corresponds to this part of the study.

3. We applied FPCA to the MNIST classification dataset. We examined the appearance of the first basis functions, the reconstructed image, and the classification quality using SVC for different numbers of components. This part of the study is represented in the notebooks/fpca_mnist.ipynb file

4. We applied FPCA to two multi-resolution image datasets - CIFAR10 and HaGRID. For both datasets, a comprehensive study was conducted regarding the required number of components in FPCA, the influence of image resolution and classification quality for different classification algorithms, and in addition, the quality metrics of the reconstructed images and their relationship with the number of components were numerically determined. The files notebooks/FPCA_multi_res.ipynb and notebooks/FPCA_multi_res_HaGRID.ipynb correspond to this part of the study

5. In the last part of the study, we studied the curse of dimensionality for FPCA. We performed a literature review on the problem, including old and new papers on covariance matrix estimation and smoothing in high-dimensional spaces, and also experimented with popular approaches to combat the curse of dimensionality on the HAM10000 dataset in the FDApy library. The file notebooks/FPCA_HAM10000.ipynb corresponds to this part of the study
