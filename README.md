# Breaking the Fake: A Neural Network-Based Fake News Detector

**Author:** Mark Vincent S. Raña  
**Institution:** College of Computer Studies, Camarines Sur Polytechnic Colleges  
**Course:** CSAC 224 – Machine Learning  
**Contact:** marana@my.cspc.edu.ph  

---

## 📌 Abstract

The spread of fake news on social media influences public opinion and political decisions, necessitating automated, high-efficiency detection methods. This study explores deep learning architectures—specifically **Bidirectional Long Short-Term Memory (LSTM)** and **1D Convolutional Neural Networks (CNN)**—to classify news articles as real or fake. Text preprocessing incorporates cleaning, tokenization, sequence padding, and word embeddings. Both architectures achieved over **99% accuracy**, demonstrating the power of neural networks in combating online misinformation.

The full academic paper is available in [`paper/Breaking_the_Fake_Paper.pdf`](paper/Breaking_the_Fake_Paper.pdf).

---

## 📊 Model Performance & Results

| Metric | Bidirectional LSTM | 1D CNN |
| :--- | :---: | :---: |
| **Accuracy** | **99.15%** | **99.52%** |
| **Precision** | 0.9885 | 0.9938 |
| **Recall** | 0.9955 | 0.9972 |
| **F1-Score** | 0.9920 | 0.9955 |

### Loss & Learning Curves
| LSTM Training Loss | CNN Training Loss |
| :---: | :---: |
| ![LSTM Loss](images/LTSM%20Model%20Loss.png) | ![CNN Loss](images/CNN%20Model%20Loss.png) |

### Confusion Matrices
| LSTM Confusion Matrix | CNN Confusion Matrix |
| :---: | :---: |
| ![LSTM Confusion Matrix](images/LSTM%20Confusion%20Matrix.png) | ![CNN Confusion Matrix](images/CNN%20Confusion%20Matrix.png) |

### ROC Curves
| LSTM ROC Curve (AUC = 1.00) | CNN ROC Curve (AUC = 1.00) |
| :---: | :---: |
| ![LSTM ROC Curve](images/LSTM%20ROC%20Curve.png) | ![CNN ROC Curve](images/CNN%20ROC%20Curve.png) |

---

## 📂 Repository Structure

```text
fake-news-detector/
├── images/                         # Training curves, ROC curves, confusion matrices
├── paper/
│   ├── Breaking_the_Fake_Paper.pdf # Full research paper
│   └── Turnitin_Similarity_Report.pdf
├── fake_news_detector.ipynb        # End-to-end Jupyter Notebook (data prep, training, eval)
├── requirements.txt                # Python environment dependencies
├── .gitignore                      # Git ignore rules (excludes large CSV files)
└── README.md                       # Project documentation
```

---

## 📥 Dataset Setup

Due to GitHub's file size limits (>100 MB combined), the raw CSV dataset files (`Fake.csv` and `True.csv`) are not committed directly to this repository.

1. Download the dataset from Kaggle:
   - [Kaggle: Fake News Detection Dataset](https://www.kaggle.com/datasets/jainpooja/fake-news-detection) or [ISOT Fake & Real News Dataset](https://www.kaggle.com/datasets/clmentbisaillon/fake-and-real-news-dataset)
2. Extract the archive and place `Fake.csv` and `True.csv` directly into the root of this project folder:
   ```text
   fake-news-detector/
   ├── Fake.csv
   ├── True.csv
   ├── fake_news_detector.ipynb
   └── ...
   ```

---

## 🚀 Getting Started

### 1. Clone the Repository
```bash
git clone https://github.com/macmac-12/fake-news-detector.git
cd fake-news-detector
```

### 2. Set Up Virtual Environment & Dependencies
```bash
python -m venv venv
# Windows (PowerShell):
.\venv\Scripts\Activate.ps1
# Linux/macOS:
source venv/bin/activate

pip install -r requirements.txt
```

### 3. Run the Notebook
```bash
jupyter notebook fake_news_detector.ipynb
```
Execute the cells sequentially to load the dataset, preprocess text, train both the LSTM and CNN models, and generate evaluation plots.
