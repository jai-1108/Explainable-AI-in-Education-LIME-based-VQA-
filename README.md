# EducationBERT — Leveraging LIME for Transparent and Accurate Visual Question Answering in Education

## Overview

This project introduces **EducationBERT**, a Visual Question Answering (VQA) system focused on educational contexts, using explainable AI techniques to enhance transparency and reliability. By integrating Local Interpretable Model-Agnostic Explanations (LIME) with Vision Transformers (ViTs), the model improves accuracy, interpretability, and user trust.

The system is designed to respond to multiple-choice questions based on image data across various educational subjects, including natural and social sciences and language arts.

## Key Features

- **Explainability with LIME**: LIME is used to create human-understandable explanations of predictions, which enhances model trust and usability in sensitive domains.
- **Vision Transformer-based Architecture**: The model uses ViTs for image processing, making it capable of handling complex visual scenarios and understanding long-range dependencies.
- **Multimodal Attention Mechanism**: Combines both visual and textual information effectively to provide accurate answers based on context.

## Dataset

The dataset contains images and multiple-choice questions focused on educational subjects:

- **Images**: Around 14,457 images are grouped into folders by question topic.
- **Questions**: Spanning various subjects like natural sciences, social studies, and grammar, with 3–5 answer options each.
- **Annotations**: Each image is paired with relevant questions and annotated with correct answers for supervised training.

You can download the dataset from [ScienceQA dataset](https://scienceqa.github.io/#dataset).

## Methodology

1. **Image Processing**: Images are preprocessed and converted into patches for the Vision Transformer.
2. **Vision Transformer Encoder**: Uses self-attention mechanisms to understand image features globally.
3. **Text Encoder**: Processes questions into high-dimensional vectors, aligning with image representations.
4. **Attention Fusion**: Merges image and text data, enabling the model to focus on relevant visual regions based on question context.
5. **Explanation and Feedback**: LIME generates explanations post-prediction, providing feedback for model refinement.

## Performance Metrics

The model is evaluated using:

- Accuracy  
- Macro F1 Score  
- Wu-Palmer Similarity (WUPS)

With LIME integrated, performance improved across all metrics:

- **Accuracy:** Increased from **62.5%** to **68.2%**  
- **Macro F1 Score:** Increased from **60.3%** to **66.7%**  
- **WUPS@0.9:** Increased from **63.8%** to **69.0%**

## Results
<img width="1470" height="620" alt="Screenshot 2025-12-06 at 11 43 50 AM" src="https://github.com/user-attachments/assets/83932a72-eeca-4072-bad3-bdc32e3ff95c" />

## Requirements

- Python 3.7+
- PyTorch
- Hugging Face Transformers
- OpenCV
- Scikit-Learn
- LIME

Install the necessary dependencies with:

```bash
pip install -r requirements.txt
