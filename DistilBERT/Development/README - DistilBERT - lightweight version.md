# DistilBERT Development - Lightweight version

_Welcome!_ This is the **lightweight** version of this model. Meaning that some heavy files (the fine tuned and regular versions of the model weights and tokens in a folder of 500mb~ each) were removed, while conserving only the notebooks and datasets. Once all of the cells are ran, the folder structure should contain all of the files and directories mentioned below.

> 💡 **Note:** This version does not include the model weights. You’ll need to run all cells to regenerate the complete folder structure.

> 💡 **Note:** Also, you may access the complete files and model weights from this [Google Drive link](https://drive.google.com/drive/folders/1l06N329qqXur4IWpec_fRk_Pgv0CetV5?usp=sharing).

This notebook presents the code to do data preprocessing tasks, load and customize the default DistilBERT model to further test it using LIAR and ReNew.

Please note, the fine tuning process is in the `./Fine Tuning Process` directory.

Important: make sure to keep the same folder structure as it comes with the corresponding ZIP file.

---

## 📰 Project Overview

This notebook loads the DistilBERT model from Huggingface, tunes it over LIAR and saves it in the `distilbert_liar_model` directory.

It also calculates important metrics such as accuracy, precision, recall, specificity, F1 Score in the following models:

- A DistilBERT model fine tuned with LIAR saved in the `distilbert_liar_model` directory.

- Preprocesses and evaluates performance on:

  - The original LIAR test set.

For further details regarding the testing results of each dataset, LIAR versus LIAR + ReNew, please refer to the `Test` directory at the root folder of this DistilBERT folder.

---

## 🏗️ Datasets Used

- **LIAR Dataset**

  - **Path**: `./LIAR dataset/test modified.tsv`
  - **Path**: `./LIAR dataset/train modified.tsv`
  - **Path**: `./LIAR dataset/valid modified.tsv`
  - **Path**: `./LIAR dataset/liar and renew mixed - training.csv`
  - **Path**: `./LIAR dataset/cleaned_test.csv`

- **ReNew Dataset**
  - **Path**: `./ReNew dataset/combined renew test.csv`
  - **Path**: `./ReNew dataset/renew false cleaned parsed (balanced version)`
  - **Path**: `./ReNew dataset/renew true cleaned parsed (balanced version)`
  - **Path**: `./ReNew dataset/true combined dataset (with titles)`

---

## ⚙️ Dependencies

Make sure the following Python libraries are installed:

```bash
pip install pandas torch scikit-learn transformers numpy tqdm seaborn matplotlib
```
