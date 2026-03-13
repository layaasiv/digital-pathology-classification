# Digital Pathology Image Classification

Fine-tuning pretrained computer vision models for tissue type classification from pathology images, with model deployment on HuggingFace Spaces.

## Tools & Technologies
- **Framework:** fastai, PyTorch
- **Models:** ConvNeXt-Large (IN22k), ConvNeXt-Tiny (IN22k), ViT-Small R26 S32
- **Deployment:** HuggingFace Spaces (Gradio)
- **Data:** Kaggle digital pathology dataset (20 tissue classes, numeric labels)

## Overview
This project fine-tunes pretrained vision models on a digital pathology image classification task. Images are labeled into 20 integer categories (0–19), each representing a different tissue type. Specific tissue identities were not provided in the dataset, which is a notable limitation for biological interpretability.

The final model was deployed as an interactive web app on HuggingFace Spaces.

🚀 **[Try the live app](https://huggingface.co/spaces/layaasiv/digital-pathology)**

## Notebooks
| Notebook | Description |
|---|---|
| `pathology-classification.ipynb` | Initial model training and baseline evaluation |
| `pathology-classification-part-2.ipynb` | Model comparison and fine-tuning experiments |
| `pathology-classification-part-3.ipynb` | Final model selection and evaluation |
| `app.ipynb` | App development and export for HuggingFace deployment |

## Models Benchmarked
| Model | Notes |
|---|---|
| ConvNeXt-Large (IN22k) | Best performing model |
| ConvNeXt-Tiny (IN22k) | Lightweight alternative |
| ViT-Small R26 S32 224 | Vision transformer baseline |

## Results
**Final accuracy: 0.96** (20-class classification)

## Limitations
- Numeric class labels (0–19) without corresponding tissue type annotations limit biological interpretability
- Single dataset source — generalizability to other pathology datasets is unknown

## Setup
```bash
conda env create -f environment.yml
conda activate <env-name>
```
Then run notebooks in order. To run the deployed app locally:
```bash
python app.py
```
