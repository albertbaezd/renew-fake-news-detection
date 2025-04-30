# XSY Albert fake news model - Lightweight version

_Welcome!_ This is the **lightweight** version of this model. Meaning that some heavy files (the fine tuned and regular versions of the model weights and tokens in a folder of 500mb~ each) were removed, while conserving only the notebooks and datasets. Once all of the cells are ran, the folder structure should contain all of the files and directories mentioned below.

> 💡 **Note:** Also, you may access the complete files and model weights from this [Google Drive link](https://drive.google.com/drive/folders/1l06N329qqXur4IWpec_fRk_Pgv0CetV5?usp=sharing).

> 💡 **Note:** This version does not include the model weights. You’ll need to run all cells to regenerate the complete folder structure. Also, if you want to run the model locally, replace the calls for the online version with an optional step of downloading the Hugging Face files for the `XSY/albert-base-v2-fakenews-discriminator` model at [the original model repository link](https://huggingface.co/XSY/albert-base-v2-fakenews-discriminator), and placing them in a folder of your preference.

These notebooks use the original and ReNew fine tuned versions of the `XSY/albert-base-v2-fakenews-discriminator` model from Hugging Face.

This is the second of our series of pre-trained models. The `XSY/albert-base-v2-fakenews-discriminator` model originally was trained over the ISOT fake news dataset available on Kaggle at `https://www.kaggle.com/datasets/clmentbisaillon/fake-and-real-news-dataset`.

Important: make sure to keep the same folder structure as it comes with the corresponding ZIP file.

---

## 📰 Project Overview

This model leverages the ISOT Fake News dataset from Kaggle, which comes from the University of Victoria, Canada. It contains long statements with over 40,000 instances on different topics.

This notebook performs data cleaning and preprocessing to match the ISOT dataset to the same format used in ReNew testing: two columns, label and statement where label is either 0 or 1.

After these changes, it evaluates the imported model in these scenarios:

- Testing the default tuned model over Politifact testing and ReNew testing.

- Testing the fine tuned model over Politifact testing and ReNew testing.

For a breakdown of additional metrics such as accuracy, precision, recall, specificity, F1 Score, please refer to the `Test` dataset, one level up inside this directory.

---

## 🏗️ Datasets Used

The merged dataset is a custom combination of the ISOT Fake News dataset that merges the true and false csv files while randomizing the order they have and removing unnecesary columns for our tests.

The Politifact dataset is the original one provided through Kaggle.

ReNew is our original dataset.

- **Dataset directory**

  - **Path**: `./dataset/LIAR_Renew_training.csv`
  - **Path**: `./dataset/renew_combined_shuffled.csv`
  - **Path**: `./dataset/renew_combined_test.csv`
  - **Path**: `./dataset/renew_combined_train.csv`

- **Politifact Dataset**

  - **Path**: `./Politifact dataset/politifact kaggle fake.csv`
  - **Path**: `./Politifact dataset/politifact kaggle true.csv`
  - **Path**: `./Politifact dataset/merged/merged_politifact_test.csv`
  - **Path**: `./Politifact dataset/merged/merged_politifact_train.csv`

- **ReNew Dataset**
  - **Path**: `./ReNew dataset/combined renew dataset.csv`
  - **Path**: `./ReNew dataset/combined renew test.csv`
  - **Path**: `./ReNew dataset/combined renew train.csv`

---

## ⚙️ Dependencies

Make sure the following Python libraries are installed:

```bash
pip install pandas torch scikit-learn transformers numpy tqdm sentencepiece protobuf accelerate
```
