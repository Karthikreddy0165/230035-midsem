# Dataset — Synthetic Time-Marked Time-Series

## Description

This directory contains the synthetic dataset used throughout the Part B notebooks.

The data is **generated programmatically** in `task_2_1.ipynb` and saved here for reproducibility.

## Dataset: `synthetic_time_marked.npz`

- **N = 20** time series (trials), each observed at **T = 50** uniformly-spaced time points.
- **K = 2** event markers per trial, sampled uniformly in [0.2, 0.8] of the trial duration.
- **True signal**: Flat before each marker, followed by an exponential response (rise then decay) — mimicking a causal event-driven process like the traffic or neural data in the paper.
- **Noise**: Additive Gaussian noise with σ = 0.3.

## How it is used

| Notebook | Usage |
|----------|-------|
| `task_2_1.ipynb` | Generates and saves the dataset |
| `task_2_2.ipynb` | Implements the time-marked GP and infers the signal |
| `task_2_3.ipynb` | Compares results and reports metrics |
| `task_3_1.ipynb` | Ablation experiments on the same dataset |
| `task_3_2.ipynb` | Failure mode analysis with noisy markers |

## Reproduction

Run `task_2_1.ipynb` from top to bottom. The random seed is set at the top of the notebook (`np.random.seed(42)`), guaranteeing identical results across runs.
