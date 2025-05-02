# ReNew (Recent News) Fake News Dataset.

*A Dataset and Model Benchmarking Project for Short Political Claims*  

## 🎯 Overview  
ReNew is a project focused on creating a manually verified dataset of short political claims scraped from renowned news classification webpages, specifically **Politifact**. The project evaluates the performance of BERT and DistilBERT models—both trained from scratch and fine-tuned—as well as pre-trained models from Hugging Face, for fake news detection. This dataset takes inspiration from the published work by: William Yang Wang. 2017. “Liar, Liar Pants on Fire”: A New Benchmark Dataset for Fake News Detection.

For access to the whole model weights and files missing in this lightweight version of the repository, please refer to: [this Google Drive link](https://drive.google.com/drive/folders/1l06N329qqXur4IWpec_fRk_Pgv0CetV5?usp=sharing).

Key phases:  
1. **Custom Model Training**:  
   - Tested BERT and DistilBERT and fine tuned them from scratch.  
   - Fine-tuned on two datasets:  
     - `LIAR` (LIAR training baseline fake news dataset).  
     - `LIAR + R` (LIAR combined with ReNew training data).  

2. **Pre-trained Model Benchmarking**:  
   - Evaluated Hugging Face's pre-trained fake news detection models in two scenarios:  
     - **Base performance** on `Politifact Test` (original test data).  
     - **Fine-tuned performance** on `ReNew Test` (our dataset).  

Evaluaed metrics for each model: Accuracy, Precision, Recall, Specificity, F1-score.  

---  
## 📂 Dataset Description  
- **ReNew Dataset**: Manually verified short political claims scraped from Politifact.  
- **LIAR**: Existing fake news dataset used for initial training.  
- **LIAR + R**: Combined dataset (LIAR + ReNew) for enhanced fine-tuning.
- **Politifact + R**: Combined dataset (Politifact + ReNew) for enhanced fine-tuning. 

---  
## 🛠️ Model Training & Evaluation  
### Models Tested  
1. **From Scratch**:  
   - BERT  
   - DistilBERT  
2. **Pre-trained (Hugging Face)**:
   - jy46604790/Fake-News-Bert-Detect. [Link](https://huggingface.co/jy46604790/Fake-News-Bert-Detect)
   - XSY/albert-base-v2-fakenews-discriminator. [Link](https://huggingface.co/XSY/albert-base-v2-fakenews-discriminator)

### Training Approach  

First, in each of the model folders, in each of the corresponding notebook files you may find the code necessary for loading the models, customizing and preprocessing the necessary datasets for that model and for performing and saving a fine tuned version of each.

### Results

Through experiments using relevant datasets such as ISOT Politifact and LIAR we were able to confirm that adding ReNew as a part of the training process of fake news detection models can improve their detection capability for recent short news statements without noticeably affecting their accuracy on the original datasets they are based on, allowing to place an additional layer of recent context on existing models for
future evaluation purposes.

<img src="https://github.com/user-attachments/assets/490487f5-2b18-42cf-a523-b126374adeeb" width="600">

<br>

<img src="https://github.com/user-attachments/assets/0a5cb703-a7df-4800-ad90-a5d989d4b4dd" width="600">


The final version of ReNew that we are presenting to the scientific community symbolizes a meaningful starting point for future research as our goal is to collaborate in a way that facilitates access for more researchers to an up-to-date multicolumn political news dataset that facilitates the exploration of new approaches in this area of study.

## 📂 Folder Structure 

    ReNew/
    ├── BERT/                                    # BERT-specific workflows
    │   ├── Development/                         # Training/fine-tuning
    │   │   ├── (model weights folder)/          # Saved weights
    │   │   ├── (notebook)/                      # Jupyter notebooks
    │   │   └── README.md                        # BERT development instructions
    │   └── Tests/                               # Model evaluation
    │       ├── (model weights folder)/          # Metrics/outputs
    │       └── README.md                        # BERT testing instructions
    │
    ├── Data_Preprocessing/     # Data cleaning/scraping
    │   ├── Development/        # Preprocessing scripts
    │   └── Tests/              # Data validation
    │       └── README.md       # Data pipeline instructions
    │
    ├── DistilBERT/             # DistilBERT-specific workflows
    │   ├── Development/        # (Same as BERT structure)
    │   └── Tests/
    │       └── README.md
    │
    ├── jy_Model/               # Custom model (e.g., "jy")
    │   ├── Development/
    │   └── Tests/
    │       └── README.md
    │
    └── XSY_Albert_Model/       # Albert-based model
        ├── Development/
        └── Tests/
            └── README.md

## 🚀 How to Reproduce  
Each model and pipeline has dedicated instructions in its subfolder:  
1. **Data Preprocessing**:  
   - See `Data Preprocessing/README - Data preprocessing split.md` for scraping/cleaning.  
2. **Model Training (Develop)**:  
   - Navigate to `[MODEL_NAME]/Development/` and follow its `README.md`.  
   - Example:  
     ```bash  
     cd BERT/Development  
     # Follow instructions to run notebooks/training scripts  
     ```  
3. **Model Testing**:  
   - Navigate to `[MODEL_NAME]/Tests/` and use its `README.md` for evaluation.  

---  
## 📄 License  
MIT License. See `LICENSE` file for details.  

---  
## 🙌 Credits  
- **Contributors**: [albertbaezd](https://github.com/albertbaezd), [Cferrer08](https://github.com/Cferrer08).  
- **Data Sources**: Politifact, LIAR dataset.  
- **Tools**: Hugging Face, PyTorch/TensorFlow, Selenium.  
