# AI Ethics Classifier (Mini ML Project)

A small, interpretable machine learning project that classifies short AI-related text statements by:

1. **AI Ethics Principle**
   - Privacy
   - Transparency
   - Accountability
   - Fairness

2. **AI Lifecycle Stage**
   - Data (collection and preprocessing)
   - Development (training and evaluation)
   - Deployment (release, monitoring, and response)

This project is designed as a learning-focused demo that turns AI ethics theory into a practical, hands-on machine learning workflow.

---

## Why this project?

AI ethics concepts are often discussed at a high level, but rarely translated into something concrete.

This project demonstrates:
- How ethical principles can be operationalized as labels
- How text classification can be used to reason about policy-like statements
- How human judgment and machine learning work together in supervised learning
- How to evaluate models using precision, recall, F1-score, and confusion matrices

The project is intentionally:
- Small
- Transparent
- Interpretable
- Easy to extend

This makes it suitable for students learning machine learning, AI ethics coursework, and portfolio demonstrations.

---

## What the model does

Given a short statement such as:

> “Evaluate model performance across demographic groups to reduce bias.”

The model predicts:
- Ethics Principle: **Fairness**
- Lifecycle Stage: **Development**

---

## Project structure

The notebook or script is organized into four main sections:

### 1. Seed labeled data
- 200 human-written examples (50 per ethics principle)
- Each example is labeled with both an ethics principle and a lifecycle stage

### 2. Interactive quiz (human-in-the-loop)
- 12 multiple-choice questions
- Ensures conceptual understanding before training
- Reinforces the meaning of each ethics principle and lifecycle stage

### 3. Model training and evaluation
- TF-IDF vectorization (unigrams and bigrams)
- Linear Support Vector Machine (LinearSVC)
- Multi-output classification (predicts two labels per statement)
- Evaluation metrics:
  - Precision
  - Recall
  - F1-score
  - Confusion matrices

### 4. Interactive testing
- Built-in test cases
- User can enter custom statements and see predicted labels

---

## Model performance (example)

With the current dataset:
- Ethics principle accuracy is approximately 75–80 percent
- Lifecycle stage accuracy is approximately 60–65 percent

Lifecycle prediction is intentionally more difficult due to overlap between stages, and even human annotators may disagree in some cases.

The focus of this project is interpretability and learning rather than production-grade accuracy.

---

## Machine learning concepts demonstrated

- Supervised learning
- Multi-class classification
- Multi-output classification
- TF-IDF text representations
- Train/test splitting and stratification
- Precision, recall, and F1-score interpretation
- Confusion matrix analysis
- Human-in-the-loop workflows

---

## How to run

### Requirements
```bash
pip install scikit-learn
