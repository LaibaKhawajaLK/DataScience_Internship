
📝 Text Summarization with BART and ROUGE Evaluation
This project demonstrates how to perform abstractive text summarization using the pretrained facebook/bart-large-cnn model from Hugging Face Transformers. It also includes evaluation of the model’s performance using the ROUGE metric.

🚀 Features
Uses BART (facebook/bart-large-cnn) for abstractive summarization.

Evaluates summaries using ROUGE-1, ROUGE-2, and ROUGE-L scores.

Implements the summarization pipeline with PyTorch backend.

Clean and simple implementation with minimal dependencies.

🛠️ Installation
Make sure you have Python ≥ 3.7. Then install the following libraries:


pip install transformers datasets evaluate rouge_score
If you're using Jupyter or Anaconda, you can install within a notebook using:


!pip install transformers datasets evaluate rouge_score
📦 Dependencies
transformers

datasets

evaluate

rouge_score

📄 Code Overview
1. Summarization using BART

from transformers import pipeline

# Load summarization pipeline
summarizer = pipeline("summarization", model="facebook/bart-large-cnn", framework="pt")

# Example usage
text = "Your long text here..."
summary = summarizer(text, max_length=130, min_length=30, do_sample=False)
print(summary[0]['summary_text'])
2. ROUGE Evaluation

import evaluate

# Load ROUGE metric
rouge = evaluate.load("rouge")

# Format data
reference_summaries = [item['reference_summary'] for item in summaries]
generated_summaries = [item['generated_summary'] for item in summaries]

# Compute and print ROUGE scores
scores = rouge.compute(predictions=generated_summaries, references=reference_summaries)

for key in scores:
    print(f"{key}: {scores[key]:.4f}")
📁 Sample Data Format

summaries = [
    {
        "reference_summary": "This is the human-written summary.",
        "generated_summary": "This is the model-generated summary."
    },
    ...
]
📊 Example Output


ROUGE Evaluation:

rouge1: 0.5213
rouge2: 0.3912
rougeL: 0.4876
✅ Use Cases
News summarization

Document distillation

Academic paper compression

Executive brief generation
