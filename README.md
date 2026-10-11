# Grokking and Fourier Circuits

Mechanistic interpretability of one-layer transformers trained on modular addition and subtraction modulo 113. The project explores learned representations through Fourier analysis, frequency ablations, activation projections, and PCA.

## Results

| Addition experiment | Test accuracy |
|---|---:|
| Baseline | 100% |
| Remove dominant frequencies (7, 15, 19) | 0.88% |
| Keep dominant frequencies and DC | 100% |

The subtraction model also achieves **100% test accuracy**, with dominant embedding frequencies at **27 and 46**. A cosine-based logit approximation preserves 100% test accuracy and explains 50.29% of logit variance.

## Usage

Open [`grokking_fourier_analysis.ipynb`](grokking_fourier_analysis.ipynb) to view the experiments and results. To run it, install dependencies using the first code cell and execute the notebook in order. Training uses CUDA when available.

## Reference

Based on [Progress measures for grokking via mechanistic interpretability](https://arxiv.org/abs/2301.05217) — Nanda et al., ICLR 2023, with additional experiments on modular subtraction.
