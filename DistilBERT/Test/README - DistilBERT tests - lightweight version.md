# DistilBERT Tests - Lightweight version

_Welcome!_ This is the **lightweight** version of this model. Meaning that some heavy files (the fine tuned and regular versions of the model weights and tokens in a folder of 500mb~ each) were removed, while conserving only the notebooks and datasets. Once all of the cells are ran, the folder structure should contain all of the files and directories mentioned below.

> 💡 **Note:** This version does not include the model weights. You’ll need to run all cells to regenerate the complete folder structure.

> 💡 **Note:** Also, you may access the complete files and model weights from this [Google Drive link](https://drive.google.com/drive/folders/1l06N329qqXur4IWpec_fRk_Pgv0CetV5?usp=sharing).

This notebook presents the code to perform tests utilizing the LIAR only fine tuned version of DistilBERT.

To see the results of the LIAR + R (LIAR testing and ReNew testing) fine tuned version of this model, please refer to the `../Development/Fine Tuning Process/distilbert fine tuning-process.ipynb` notebook.

Important: make sure to keep the same folder structure as it comes with the corresponding ZIP file.

---

## 📰 Project Overview

This notebook loads the LIAR only finetuned version of DistilBERT and further tests its performance in the LIAR testing and ReNew testing datasets.

It also calculates important metrics such as accuracy, precision, recall, specificity, F1 Score in the following cases:

- A DistilBERT model fine tuned with LIAR saved in the `Model` directory.

Uses an specific set of parameters to balance performance and testing time.

---

## 🏗️ Datasets Used

Uses datasets located in the `./data` route.

- **LIAR Dataset**

  - **Path**: `./data/test_modified.tsv`

- **ReNew Dataset**
  - **Path**: `./data/renew_combined_test.csv`

---

## ⚙️ Dependencies

Make sure the following Python libraries are installed:

```bash
pip install pandas torch scikit-learn transformers numpy tqdm
```
