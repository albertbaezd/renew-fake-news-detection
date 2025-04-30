# jy46 Hugging Face Model Development - Lightweight version

_Welcome!_ This is the **lightweight** version of this model. Meaning that some heavy files (the fine tuned and regular versions of the model weights and tokens in a folder of 500mb~ each) were removed, while conserving only the notebooks and datasets. Once all of the cells are ran, the folder structure should contain all of the files and directories mentioned below.

> 💡 **Note:** Also, you may access the complete files and model weights from this [Google Drive link](https://drive.google.com/drive/folders/1l06N329qqXur4IWpec_fRk_Pgv0CetV5?usp=sharing).

> 💡 **Note:** This version does not include the model weights. You’ll need to run all cells to regenerate the complete folder structure. Also, an additional step of downloading the Hugging Face files for the `jy46604790/Fake-News-Bert-Detect` model at [the original model repository link](https://huggingface.co/jy46604790/Fake-News-Bert-Detect), and place them inside a folder titled `jy46604790_fake_news_bert_detect` at the same level as the ipynb files.

These notebooks use the original and ReNew fine tuned versions of the `jy46604790/Fake-News-Bert-Detect` model from Hugging Face.

This is the first of our series of pre-trained models. The `jy46604790/Fake-News-Bert-Detect` model originally was trained over the ISOT fake news dataset available on Kaggle at `https://www.kaggle.com/datasets/clmentbisaillon/fake-and-real-news-dataset`.

Important: make sure to keep the same folder structure as it comes with the corresponding ZIP file.

---

## 📰 Project Overview

This model leverages the ISOT Fake News dataset from Kaggle, which comes from the University of Victoria, Canada. It contains long statements with over 40,000 instances on different topics.

The first notebook, `jyBaseModelTests.ipynb` loads the default model as it comes from Hugging Face, stored in the `./jy46604790_fake_news_bert_detect` directory.

It also calculates important metrics such as accuracy, precision, recall, specificity, F1 Score in the following cases:

- Testing the default tuned model over Politifact testing.

- Testing the default tuned model over ReNew testing.

The second notebook, `jyFineTunedTests.ipynb` loads the fine tuned model, stored in the `./finetuned_models/jy46_fine_tuned_fake_news_bert` directory.

Then, it calculates important metrics such as accuracy, precision, recall, specificity, F1 Score in the following cases:

- Testing the fine tuned tuned model over Politifact testing.

- Testing the fine tuned tuned model over ReNew testing.

---

## 🏗️ Datasets Used

- **Politifact Dataset**

  - **Path**: `./politifact/merged_politifact_test.csv`
  - **Path**: `./politifact/merged_politifact_train.csv`

- **ReNew Dataset**
  - **Path**: `./Cleaned dataset/renew/combined/combined renew test.csv`
  - **Path**: `./Cleaned dataset/renew/combined/combined renew dataset.csv`
  - **Path**: `./Cleaned dataset/renew/combined/combined renew train.csv`

---

## ⚙️ Dependencies

Make sure the following Python libraries are installed:

```bash
pip install pandas torch scikit-learn transformers numpy tqdm
```
