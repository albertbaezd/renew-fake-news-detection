# BERT Model Results - Showcase - Lightweight version

_Welcome!_ This is the **lightweight** version of this model. Meaning that some heavy files (the fine tuned and regular versions of the model weights and tokens in a folder of 500mb~ each) were removed, while conserving only the notebooks and datasets. Once all of the cells are ran, the folder structure should contain all of the files and directories mentioned below.

> 💡 **Note:** This version does not include the model weights. You’ll need to run all cells to regenerate the complete folder structure.

> 💡 **Note:** Also, you may access the complete files and model weights from this [Google Drive link](https://drive.google.com/drive/folders/1l06N329qqXur4IWpec_fRk_Pgv0CetV5?usp=sharing).

This notebook presents evaluation results for a BERT model fine-tuned on the LIAR and RENEW dataset and tested on various datasets to assess its generalization performance.

It compares the performance of LIAR versus LIAR + R (Where R = ReNew, our novel fake news detection dataset).

Important: make sure to keep the same folder structure as it comes with the corresponding ZIP file.

---

## 📰 Project Overview

This notebook shows metrics such as accuracy, precision, recall, specificity, F1 Score in the following models:

- A BERT model fine tuned with LIAR from the `./bert_liar_model` directory.
- Preprocesses and evaluates performance on:

  - The original LIAR test set.
  - The ReNew test set

- A BERT model fine tuned with ReNew and LIAR from the `./fine tuned models/bert_renew_combined_finetuned_model` directory.
- Preprocesses and evaluates performance on:
  - The original LIAR test set.
  - The ReNew test set

---

## 🏗️ Datasets Used

- **LIAR Dataset**

  - **Path**: `./LIAR dataset/test modified.tsv`
  - **Preprocessing**: Maps `"TRUE"` and `"mostly-true"` to label `1`; all others to `0`.

- **ReNew Dataset**
  - **Path**: `./ReNew dataset/combined renew test.csv`

---

## ⚙️ Dependencies

Make sure the following Python libraries are installed:

```bash
pip install pandas torch scikit-learn transformers numpy
```
