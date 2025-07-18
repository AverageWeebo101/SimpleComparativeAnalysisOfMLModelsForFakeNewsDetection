# SimpleComparativeAnalysisOfMLModelsForFakeNewsDetection - Setup Guide

This guide helps you set up the environment and run the Jupyter notebook, uwu.

## Prerequisites
- **Python 3.7+** (Install from [python.org](https://python.org))
- **VS Code** with extensions:
  - *Jupyter Notebook* (official Microsoft extension)
  - *Python* (official Microsoft extension)
- **Kaggle Account** ([Sign up here](https://kaggle.com))

## Kaggle API Setup
1. Go to your Kaggle Account Settings
2. Click "Create New API Token" → Downloads kaggle.json
3. Place kaggle.json in the project root directory

## Initial Setup

### 1. Clone Repository
```bash
git clone https://github.com/AverageWeebo101/SimpleComparativeAnalysisOfMLModelsForFakeNewsDetection.git
cd project-repo
```

## 2. Create Virtual Environment
```bash
python -m venv .venv
```

## 3. Activate Environment
For Windows:
```bash
.\.venv\Scripts\activate
```

## 4. Install Dependencies
```bash
pip install numpy pandas scikit-learn tensorflow transformers matplotlib seaborn kaggle
```

## Dataset is downloaded automnatically, as long as you have kaggle.json in project root directory
