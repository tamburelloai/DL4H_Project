# **Combining Structured and Unstructured Data for Predictive Models: A Deep Learning Approach**

---
#### NOTE: This is a reproduction of original work by Dongdong Zhang, Changchang Yin, Jucheng Zeng, Xiaohui Yuan, and Ping Zhang.
Original Repository: [https://github.com/onlyzdd/clinical-fusion](https://github.com/onlyzdd/clinical-fusion)

---

This repository is part of a course project for **Deep Learning for Healthcare**. The project is based on the original work titled "Combining structured and unstructured data for predictive models: a deep learning approach" by Dongdong Zhang, Changchang Yin, Jucheng Zeng, Xiaohui Yuan, and Ping Zhang. This study presents an innovative approach to predictive modeling in healthcare by fusing structured and unstructured Electronic Health Records (EHRs) through deep learning techniques.

## **Introduction**
The original paper proposes multi-modal neural network architectures designed to integrate sequential unstructured notes with structured clinical data. By utilizing document embeddings, convolutional neural networks (CNNs), and long short-term memory (LSTM) networks, these models aim to improve the representation of patient data. The paper demonstrates significant improvements in predicting in-hospital mortality, 30-day hospital readmission, and length of stay, showcasing the potential of combined data approaches over traditional single-data-type models.

### **Data download instruction**

To obtain the dataset (MIMIC-III) follow the official instructions at https://mimic.physionet.org/gettingstarted/access/.

You will then need to run sql commands in order to generate multiple tables of which you will use BigQuery or a local SQL database to do so. Next, you will place the resulting tables (saved as .csv files) under data/mimic in the root of wherever you run this.


- Follow the instructions at https://github.com/MIT-LCP/mimic-code/tree/master/buildmimic/postgres.
- Run SQL queries to generate necessary views:
1. follow the authors instructions: https://github.com/onlyzdd/clinical-fusion/tree/master/query.

or
2. Run the SQL commands in within the notebook (.ipynb) after establishing a client connection to BigQuery.


## **Scope of Reproducibility**
In this project, we aim to reproduce the findings of the original paper under the following two hypotheses:

### **Hypothesis 1: Fusion Models Outperform Single-Data-Type Models**
- **Null Hypothesis (H0):**
  - Fusion models do not outperform models that solely use structured or unstructured data.
- **Alternative Hypothesis (H1):**
  - Fusion models significantly outperform single-data-type models in predictive accuracy for critical healthcare outcomes.

### **Hypothesis 2: Deep Learning Techniques Are Effective for Data Fusion**
- **Null Hypothesis (H0):**
  - Deep learning techniques offer no significant advantage over traditional methods in data fusion.
- **Alternative Hypothesis (H1):**
  - CNNs and LSTMs significantly enhance predictive modeling through effective data fusion, improving patient representation and outcome prediction.

## **Reproduction Efforts**
This reproduction effort was heavily focused on data processing due to the multimodal nature of the datasets. The process involved preparing, cleaning, and integrating structured and unstructured data. Although the data preparation was time-consuming, the rest of the reproduction process was straightforward with no major issues encountered.

## **Results**
The outcomes of our reproduction efforts align with the findings of the original author. Our results confirmed the effectiveness of fusion models, demonstrating enhanced predictive accuracy in critical healthcare outcomes compared to single-data-type models.

## **Conclusions**
Our findings support the original conclusions that deep learning techniques, specifically CNNs and LSTMs, are effective in combining structured and unstructured healthcare data. This approach significantly improves the predictive accuracy of outcomes such as in-hospital mortality, readmission rates, and length of stay. These results are promising for the future of healthcare informatics and predictive modeling.

## **Acknowledgments**
I would like to thank our course instructors and peers for their guidance and insights during this project. Special thanks to the original authors for their groundbreaking work and for providing access to their models and data.

