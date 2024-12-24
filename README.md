# NPL-Sentinel

![NPL Sentinel Banner](images/sentinel_banner.png)

- ▶️ [Vídeo da Apresentação](https://drive.google.com/file/d/1TIxEj9jhdVLBvoXU1iSPaHxqvGfuRkXf/view?usp=sharing) (15 min)
- 📂 [Link Apresentação](https://docs.google.com/presentation/d/1GoP6OIU4CO6ypWyeoN47Ye6HG4E-Hq_R/edit?usp=sharing&ouid=114780034926001489401&rtpof=true&sd=true) (PPT)

## Table of Contents

1. [Project Overview](#project-overview)
2. [Objectives](#objectives)
3. [Models and Approaches](#models-and-approaches)
4. [Data Description](#data-description)
5. [Sample Data](#sample-data)
6. [Running the Project](#running-the-project)
7. [Repository Structure](#repository-structure)
8. [Results and Performance](#results-and-performance)
   - [Classical & Neural Models (SVM, BERT)](#classical--neural-models-svm-bert)
   - [LLM In-Context Learning (OpenAI and Google Gemini)](#llm-in-context-learning-openai-and-google-gemini)
9. [Contributions](#contributions)

---

## Project Overview

**NPL-Sentinel** is a Natural Language Processing (NLP) project focused on **sentiment analysis** of consumer product reviews. While the models implemented here do not target maximum predictive accuracy, the main goal is to explore and apply NLP training techniques and methodologies to a realistic scenario—analyzing consumer sentiments toward a smartphone product.

The name **NPL-Sentinel** conveys the idea of a "sentinel" continuously monitoring opinions to uncover trends and insights that drive informed decision-making.

---

## Objectives

1. **Sentiment Classification:** Identify whether a given product review is positive, neutral, or negative.
2. **Rating Correlation:** Examine the relationship between sentiment polarity and the consumers’ numerical ratings.
3. **Exploratory Analysis:** Identify prominent words, entities, bigrams, trigrams, and patterns in textual data.
4. **Model Comparison:** Compare the performance of various models, including classical machine learning approaches, transformer-based models (BERT), and Large Language Models (LLMs) via In-Context Learning.

---

## Models and Approaches

- **SVM + Bag of Words (BoW):** Classic machine learning approach using simple text vectorization.
- **SVM + Embeddings (spaCy):** Using pre-trained Portuguese embeddings for semantic representation.
- **BERT (Fine-tuned):** Adapting a pre-trained BERT model (Portuguese) for sentiment classification.
- **In-Context Learning with LLMs:** Zero or few-shot classification using:
  - **OpenAI GPT-4o**
  - **Google Gemini**

---

## Data Description

The dataset consists of:

- **review:** A free-form text evaluation of the smartphone.
- **rating (1 to 5):** A numerical score reflecting consumer satisfaction.

From the rating, we derive sentiment labels as follows:

- Rating ≥ 4 → Positive
- Rating ≤ 2 → Negative
- Rating = 3 → Neutral

---

## Sample Data

Below are some example entries from the dataset (`reviews.csv`):

| review                                                                                   | rating |
| ---------------------------------------------------------------------------------------- | ------ |
| "O produto é ok, nada demais. não se destaca no mercado."                                | 3      |
| "Decepcionante, não atendeu às expectativas."                                            | 1      |
| "Não tenho muito o que comentar, cumpre o que promete."                                  | 2      |
| "Gostei bastante, mas poderia ter mais funcionalidades."                                 | 4      |
| "Excelente serviço, estou muito satisfeito porque atendeu todas as minhas expectativas." | 5      |

---

## Running the Project

This project is designed to run in **Google Colab**, not locally. Use the following placeholder link to open the notebook in Colab:

**[Run in Google Colab](https://colab.research.google.com/drive/1TpvhAvSCIUNvpEGziY5FV3MKKqE0u_5T?usp=sharing)**

Before running:

- Ensure that you have access to the necessary data files as described in the notebook.
- All required libraries are installed within the notebook.
- Generate and securely store your OpenAI and Google Gemini API keys as secrets in Google Colab.

---

## Repository Structure

The repository is organized as follows:

```bash
npl-sentinel/
├─ data/
│  └─ reviews.csv
├─ images/
│  └─ sentinel_banner.png
├─ notebook/
│  └─ Pos_Deep_Learning_Projeto_NPL_Sentinel_22_Dez_2024.ipynb
├─ python-src/
│  └─ pos_deep_learning_projeto_npl_sentinel_22_dez_2024.py
├─ .gitignore
├─ LICENSE
├─ Project NLP.pdf
└─ README.md
```

**Key Files:**

- **[data/reviews.csv](data/reviews.csv)**: Contains the product reviews and corresponding ratings.
- **[images/sentinel_banner.png](images/sentinel_banner.png)**: Banner image for the project.
- **[notebook/Projeto_NPL_Sentinel_15_Dez_2024.ipynb](notebook/Projeto_NPL_Sentinel_15_Dez_2024.ipynb)**: Main Colab notebook with all code and analyses.
- **[src/projeto_npl_sentinel_15_dez_2024.py](src/projeto_npl_sentinel_15_dez_2024.py)**: Python script with project-related code.

---

## Results and Performance

### Classical & Neural Models (SVM, BERT)

| Model              | Accuracy | F1-Score |
| ------------------ | -------- | -------- |
| SVM + Bag of Words | 0.523013 | 0.477371 |
| SVM + Embeddings   | 0.539749 | 0.487158 |
| BERT               | 0.602510 | 0.580334 |

**Key Observation:**
Although not primarily focused on maximizing accuracy, BERT outperformed the SVM-based methods, achieving the highest accuracy and F1-Score among the tested models.

---

### LLM In-Context Learning (OpenAI and Google Gemini)

**OpenAI GPT-4o Evaluation (Sampled Set):**

- Correct Classifications: 10/10 (100% accuracy for sampled set)

**Google Gemini Evaluation (Sampled Set):**

- Correct Classifications: 8/10 (80% accuracy for sampled set)

---

## Contributions

- **Authors:**
  - Paloma Corrêa Alves (`pca2@cin.ufpe.br`)
  - Luciano Ayres Farias de Carvalho (`lafc@cin.ufpe.br`)

This project was developed as part of a **post-graduate** Deep Learning course at CIn - UFPE, under the supervision of Professor Luciano Barbosa.

**NPL-Sentinel** serves as a foundation for exploring and applying NLP techniques to a product-related sentiment analysis scenario. While high accuracy was not the main goal, these experiments provide a valuable learning experience and can be extended to other domains, languages, and more complex sentiment tasks.
