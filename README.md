# GRACE Terrestrial Water Storage Downscaling Framework

A spatiotemporal deep learning framework integrating CNN-BiLSTM with attention mechanisms for enhancing GRACE satellite data resolution from 1° to 0.1°.

## Key Features
- Hybrid CNN-BiLSTM architecture with spatiotemporal attention
- Bayesian optimization for hyperparameter tuning
- Automated data preprocessing pipeline
- Hydrological consistency validation modules
- Drought monitoring integration (GRACE-DSI/SPEI)

## System Requirements

### Hardware
| Component      | Minimum              | Recommended         |
|----------------|----------------------|---------------------|
| RAM            | 16 GB DDR4           | 32 GB DDR4          |
| GPU            | NVIDIA GTX 1060 (4GB)| NVIDIA RTX 3090 (24GB)|
| Storage        | 50 GB HDD            | 500 GB NVMe SSD     |

### Software
- **MATLAB 2023a** or newer with:
- Deep Learning Toolbox
- Statistics and Machine Learning Toolbox
- Parallel Computing Toolbox

## Dataset Requirements
### Mandatory Input Structure
| Variable      | Units  | Description                 |
|---------------|--------|-----------------------------|
| SM, ET, VCW... | mm     | hydrological predictors  |
TWSA          | cm     | Target variable             |

## Execution Pipeline
1.  Data Preparation
2.  Preprocessing:  `main.m`
3.  Model Training: Execute `CNN_BiLSTM_BayesOpt.m`
4.  Results : Run `plot_results.ipynb`
