# Simple Comparative Analysis of Machine Learning Models for Fake News Detection

## Project Description
This repository contains a comparative analysis of four machine learning approaches (Logistic Regression, Random Forest, LSTM, and DistilBERT) for fake news classification. Developed as partial fulfillment for CS20L (12044) Summer School Year 2025.

## Background: The Challenge of Fake News
Fake news represents a significant threat to information ecosystems worldwide. Defined as "fabricated information that mimics news media content in form but not in organizational process or intent" (Lazer et al., 2018), it undermines democratic processes (Allcott & Gentzkow, 2017) and public health responses (Wang et al., 2019). Key characteristics include:
- Deliberate spread of misinformation
- Emotional manipulation (Vosoughi et al., 2018)
- Exploitation of cognitive biases (Pennycook & Rand, 2019)

*Academic References:*  
[1] Lazer, D. M., et al. (2018). The science of fake news. *Science*, 359(6380), 1094-1096.  
[2] Allcott, H., & Gentzkow, M. (2017). Social media and fake news in the 2016 election. *Journal of Economic Perspectives*, 31(2), 211-36.  
[3] Vosoughi, S., et al. (2018). The spread of true and false news online. *Science*, 359(6380), 1146-1151.  
[4] Pennycook, G., & Rand, D. G. (2019). Fighting misinformation on social media using crowdsourced judgments of news source quality. *PNAS*, 116(7), 2521-2526.  

## Selected Models & Rationale
We compare four distinct modeling approaches representing different complexity levels:

### 1. Logistic Regression (LR)
- **What**: Simple linear classifier
- **Why**: Baseline model for interpretability and computational efficiency
- **Strengths**: Fast training, clear feature importance

### 2. Random Forest (RF)
- **What**: Ensemble of decision trees
- **Why**: Handles non-linear relationships without extensive tuning
- **Strengths**: Robust to overfitting, handles mixed features

### 3. LSTM (Long Short-Term Memory)
- **What**: Recurrent Neural Network variant
- **Why**: Captures sequential dependencies in text
- **Strengths**: Models contextual relationships in sentences

### 4. DistilBERT
- **What**: Distilled version of BERT (Transformer-based)
- **Why**: State-of-the-art NLP performance with 40% fewer parameters
- **Strengths**: Contextual word embeddings, transfer learning capabilities

*Progression Rationale*: This selection provides a gradient from simple (LR) to complex (Transformer) models, allowing performance-computation tradeoff analysis.

## Dataset
[Fake and Real News Dataset](https://www.kaggle.com/datasets/clmentbisaillon/fake-and-real-news-dataset)  
- **Fake news**: 23,481 articles  
- **Real news**: 21,417 articles  
- **Features**: Title, text, subject, date  

## Critical Limitations & Caveats

### 1. Computational Constraints
- **Hardware Limitations**: Models were trained on consumer-grade laptops (no GPU acceleration)
- **Optimization Focus**: Prioritized training efficiency over hyperparameter tuning
- **Consequences**:
  - Reduced model complexity (especially for LSTM/DistilBERT)
  - Suboptimal parameter selection
  - Smaller sample sizes for deep learning models

### 2. Problem Simplification
- **Binary Classification Limitation**: Real-world misinformation exists on a spectrum (satire, bias, manipulation)
- **"Fake News" Overgeneralization**: The term risks oversimplifying diverse misinformation types (Tandoc et al., 2018)
- **Linguistic Complexity**: Models struggle with sarcasm, cultural context, and emerging tactics

*Reference:*  
[5] Tandoc, E. C., et al. (2018). Defining 'fake news'. *Digital Journalism*, 6(2), 137-153.

### 3. Additional Constraints
- **Temporal Decay**: Models not evaluated against novel disinformation tactics
- **Feature Extraction**: Limited semantic feature engineering
- **Evaluation Metrics**: Focused on accuracy/F1 without deception-specific metrics

## Ethical Considerations
**Use with caution** - Never deploy such systems without:
- Human oversight loops
- Regular adversarial testing
- Transparency about false positive rates
- Contextual understanding of local information ecosystems
