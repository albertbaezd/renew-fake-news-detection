# XSY Albert fake news model - Lightweight version

_Welcome!_ This is the **lightweight** version of this model. Meaning that some heavy files (the fine tuned and regular versions of the model weights and tokens in a folder of 500mb~ each) were removed, while conserving only the notebooks and datasets. Once all of the cells are ran, the folder structure should contain all of the files and directories mentioned below.

> 💡 **Note:** Also, you may access the complete files and model weights from this [Google Drive link](https://drive.google.com/drive/folders/1l06N329qqXur4IWpec_fRk_Pgv0CetV5?usp=sharing).

> 💡 **Note:** This version does not include the model weights. You’ll need to run all cells to regenerate the complete folder structure. Also, if you want to run the model locally, there's an additioanl step of downloading the Hugging Face files for the `XSY/albert-base-v2-fakenews-discriminator` model at [the original model repository link](https://huggingface.co/XSY/albert-base-v2-fakenews-discriminator), and placing them in a folder named `model` at the same level as the notebooks (.ipynb) files here.

These notebooks use the original and ReNew fine tuned versions of the `XSY/albert-base-v2-fakenews-discriminator` model from Hugging Face.

This is the second of our series of pre-trained models. The `XSY/albert-base-v2-fakenews-discriminator` model originally was trained over the ISOT fake news dataset available on Kaggle at `https://www.kaggle.com/datasets/clmentbisaillon/fake-and-real-news-dataset`.

Important: make sure to keep the same folder structure as it comes with the corresponding ZIP file.

---

## 📰 Project Overview

This model leverages the ISOT Fake News dataset from Kaggle, which comes from the University of Victoria, Canada. It contains long statements with over 40,000 instances on different topics.

The first notebook, `XSYalbert_Test.ipynb` loads the default model as it comes from Hugging Face, stored in the `./model` directory.

It also calculates important metrics such as accuracy, precision, recall, specificity, F1 Score in the following cases:

- Testing the default tuned model over Politifact testing.

- Testing the default tuned model over ReNew testing.

The second notebook, `XSYalbert_Finetuned_Test.ipynb` loads the fine tuned model, stored in the `./finetuned-model` directory.

Then, it calculates important metrics such as accuracy, precision, recall, specificity, F1 Score in the following cases:

- Testing the fine tuned tuned model over Politifact testing.

- Testing the fine tuned tuned model over ReNew testing.

---

## 🏗️ Datasets Used

The merged dataset is a custom combination of the ISOT Fake News dataset that merges the true and false csv files while randomizing the order they have and removing unnecesary columns for our tests.

These datasets are located inside the `./data` directory.

- **Politifact Dataset**

  - **Path**: `./data/politifact/merged_politifact_test.csv`

- **ReNew Dataset**
  - **Path**: `./data/renew/combined renew test.csv`
  - **Path**: `./data/renew/combined renew train.csv`
  - **Path**: `./data/renew/combined renew dataset.csv`

---

## ⚙️ Dependencies

Make sure the following Python libraries are installed:

```bash
pip install pandas torch scikit-learn transformers numpy tqdm
```
