# TOPSIS for Selecting the Best Pre-trained Text Summarization Model

## Overview
This project applies the **TOPSIS (Technique for Order Preference by Similarity to Ideal Solution)** method to select the best **pre-trained text summarization model**. The evaluation is based on ROUGE scores (ROUGE-1, ROUGE-2, and ROUGE-L) to measure the effectiveness of each model.

## Models Evaluated
The following pre-trained models from Hugging Face were used:
- `facebook/bart-large-cnn`
- `google/pegasus-xsum`
- `t5-small`
- `sshleifer/distilbart-cnn-12-6`

## Steps Involved
1. **Summarization**: Generate summaries using different models.
2. **Evaluation**: Compute ROUGE-1, ROUGE-2, and ROUGE-L scores.
3. **Normalization**: Apply Min-Max scaling to scores.
4. **TOPSIS Calculation**:
   - Compute Euclidean distances from the ideal best and worst values.
   - Compute TOPSIS scores.
   - Rank models based on the highest TOPSIS score.
5. **Visualization**:
   - Generate a bar chart comparing TOPSIS scores.
   - Display results in tabular format.

## Installation
Run the following command to install the required dependencies:
```bash
pip install transformers numpy pandas scikit-learn rouge-score matplotlib seaborn
```

## Usage
Run the script using:
```bash
python topsis_text_summarization.py
```

## Expected Output
- **Table with ROUGE Scores, TOPSIS Scores, and Ranking**
- **Graph comparing the TOPSIS scores of different models**
- **Final selection of the best text summarization model**

## Results Interpretation
The model with the **highest TOPSIS score** is the best-performing model based on the given evaluation criteria.

## Contribution
- Modify the script to include additional models if required.
- Change the sample text and ground-truth summary for different domains.
- Improve evaluation by adding other metrics like BLEU or METEOR.

## License
This project is for academic purposes and is free to use under an open-source license.

