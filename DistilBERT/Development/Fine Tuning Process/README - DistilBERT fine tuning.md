# DistilBERT Fine Tuning

This notebook is a continuation of the previous notebook. Here, we will perform fine tuning operations over the DistilBERT model to add an additional layer of data training, thus creating the DistilBERT (LIAR + R) fine tuned version.

Important: make sure to keep the same folder structure as it comes with the corresponding ZIP file.

---

## 📰 Project Overview

The dataset used for this notebook is a combination between LIAR (training) and ReNew (Training) shuffled and in randomized order to help the model better generalize in either recent or old news statements.

This notebook loads the DistilBERT model from Huggingface, tunes it over LIAR + R and saves it in the `./fine tuned/distilbert_liar_renew_model` directory.

It also calculates important metrics such as accuracy, precision, recall, specificity, F1 Score in the following cases:

- Testing the fine tuned model over LIAR testing.

- Testing the fine tuned model over ReNew testing.

For further details regarding the testing results of each dataset, LIAR versus LIAR + ReNew, please refer to the `Test` directory at the root folder of this DistilBERT folder.

---

## 🏗️ Datasets Used

- **LIAR Dataset**

  - **Path**: `./LIAR dataset/cleaned for training/cleaned_test.csv`
  - **Path**: `./LIAR dataset/cleaned for training/cleaned_train.csv`
  - **Path**: `./LIAR dataset/combined liar and renew/liar and renew test.csv`
  - **Path**: `./LIAR dataset/combined liar and renew/liar and renew training.csv`

- **ReNew Dataset**
  - **Path**: `./ReNew/combined renew test.csv`
  - **Path**: `./ReNew/combined renew dataset.csv`
  - **Path**: `./ReNew/combined renew train.csv`

---

## ⚙️ Dependencies

Make sure the following Python libraries are installed:

```bash
pip install pandas torch scikit-learn transformers numpy tqdm
```
