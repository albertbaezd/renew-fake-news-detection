# jy46 Hugging Face Model Development - Lightweight version

_Welcome!_ This is the **lightweight** version of this model. Meaning that some heavy files (the fine tuned and regular versions of the model weights and tokens in a folder of 500mb~ each) were removed, while conserving only the notebooks and datasets. Once all of the cells are ran, the folder structure should contain all of the files and directories mentioned below.

> 💡 **Note:** Also, you may access the complete files and model weights from this [Google Drive link](https://drive.google.com/drive/folders/1l06N329qqXur4IWpec_fRk_Pgv0CetV5?usp=sharing).

> 💡 **Note:** This version does not include the model weights. You’ll need to run all cells to regenerate the complete folder structure. Also, an additional step of downloading the Hugging Face files for the `jy46604790/Fake-News-Bert-Detect` model at [the original model repository link](https://huggingface.co/jy46604790/Fake-News-Bert-Detect), and place them inside a folder titled `jy46604790_fake_news_bert_detect` at the same level as the ipynb file.

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

This notebook uses the original version of the `jy46604790/Fake-News-Bert-Detect` model from Hugging Face and creates a new fine tuned version saved in `./fine tuned models/jy46_fine_tuned_fake_news_bert`.

This is the first of our series of pre-trained models. The `jy46604790/Fake-News-Bert-Detect` model originally was trained over the ISOT fake news dataset available on Kaggle at `https://www.kaggle.com/datasets/clmentbisaillon/fake-and-real-news-dataset`.

Important: make sure to keep the same folder structure as it comes with the corresponding ZIP file.

---

## 📰 Project Overview

This model leverages the ISOT Fake News dataset from Kaggle, which comes from the University of Victoria, Canada. It contains long statements with over 40,000 instances on different topics.

Applies data transformation operations such as tokenization operations and mapping labels from categorical values to 0 and 1 for easier management.

For further metrics, and a more in depth comparison of the results, please navigate one level back and refer to the `Test` folder which contains the tests made over the Politifact Test and ReNew Test datasets.

---

## 🏗️ Datasets Used

- **Politifact Dataset**

  - **Path**: `./Politifact dataset/politifact kaggle fake.csv`
  - **Path**: `./Politifact dataset/politifact kaggle true.csv`
  - **Path**: `./Politifact dataset/merged/merged_politifact_test.csv`
  - **Path**: `./Politifact dataset/merged/merged_politifact_train.csv`

- **ReNew Dataset**
  - **Path**: `./ReNew dataset/combined renew test.csv`

---

## ⚙️ Dependencies

Make sure the following Python libraries are installed:

```bash
pip install pandas torch scikit-learn transformers numpy
```
