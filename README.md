# Patronizing and Condescending Language (PCL) Detection

This project implements binary classification for detecting Patronizing and Condescending Language (PCL) using a fine-tuned DeBERTa model, based on the "Don't Patronize Me!" dataset from SemEval-2022 Task 4.

## Project Structure

```
├── exercise1.md          # Paper analysis and critique
├── exercise2.ipynb       # Exploratory Data Analysis (EDA)
├── exercise3.ipynb       # DeBERTa model training and evaluation
├── exercise3.md          # Proposed approach documentation
├── error_analysis.ipynb  # Comprehensive error analysis
├── data/                 # Dataset files
└── models/               # Trained model checkpoints
```

## Exercises

### Exercise 1: Paper Analysis
Critical analysis of the original "Don't Patronize Me!" paper, covering:
- Primary contributions
- Technical strengths
- Key weaknesses and areas for improvement

### Exercise 2: Exploratory Data Analysis
Comprehensive EDA including:
- Label distribution analysis (90.5% non-PCL, 9.5% PCL)
- Keyword-label associations
- Text length and word count statistics
- N-gram frequency analysis
- Stop word density analysis
- UMAP embedding visualization

### Exercise 3: Model Training
Fine-tuned DeBERTa-base model with:
- Weighted random sampling to handle class imbalance
- Early stopping with patience=3
- Binary classification (PCL vs non-PCL)
- **Best F1 Score: 0.6184** on dev set

### Error Analysis
Detailed analysis of model performance:
- Confusion matrix visualization
- False positive/negative analysis
- Performance by text length and keyword
- ROC and Precision-Recall curves
- ROC AUC: 0.9053, PR AUC: 0.5728

## Requirements

Key dependencies:
- Python 3.10+
- PyTorch
- Transformers (HuggingFace)
- scikit-learn
- pandas, numpy
- matplotlib, seaborn
- UMAP-learn

Install dependencies:
```bash
pip install -r requirements.txt
```

## Usage

1. **Run EDA**: Open and execute `exercise2.ipynb`
2. **Train Model**: Execute `exercise3.ipynb` to train the DeBERTa model
3. **Analyze Errors**: Run `error_analysis.ipynb` for detailed performance analysis

## Dataset

Uses the "Don't Patronize Me!" dataset containing 10,469 paragraphs from news articles about vulnerable communities. Labels range from 0-4, converted to binary (PCL: >1, non-PCL: <=1).

## Results

| Metric | Value |
|--------|-------|
| F1 Score | 0.6184 |
| Precision | 0.60 |
| Recall | 0.64 |
| Accuracy | 0.92 |
| ROC AUC | 0.9053 |
# NLP-DPM
