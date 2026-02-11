# PhishGuard: Real-Time Bangla SMS Phishing Detector

I built PhishGuard because phishing SMS attacks are getting way too common in Bangladesh—people losing money from fake bank alerts, OTP scams, suspicious links, you name it. This tool analyzes Bangla SMS in real time and flags whether it's **phishing** or **legitimate**.

## 🎯 Why This Project Exists

Most phishing detection systems are designed primarily for English text. However, Bangla-speaking users are often targeted through localized scam messages that traditional detection systems fail to identify.

This project attempts to bridge that gap by building a phishing detection system specifically tailored for Bangla SMS content.

---

It's a full ML project with a custom dataset I collected and labeled myself, and it hits **100% accuracy** on the test set. Pretty satisfying result!

### 🚀 Key Features
- Bangla-specific text preprocessing (stopword removal, stemming, normalization)
- Multiple models working together:
  - K-Means for clustering and pattern discovery
  - Apriori for finding frequent phishing phrases
  - HMM for sequence modeling
  - SVM for solid classification
  - CNN for deep text feature extraction
- Streamlit web app — just paste an SMS and get instant prediction
- Custom dataset: 100% Bangla real-world SMS (phishing + normal examples)

### 📊 Quick Project Overview
I started by collecting real Bangla SMS examples (from Google Sheet), labeled them manually, then went through the usual pipeline:
1. Data collection & labeling
2. Cleaning and Bangla text preprocessing
3. EDA + clustering
4. Feature engineering with Apriori patterns
5. Training models: HMM, SVM, CNN
6. Evaluation (confusion matrix, accuracy, precision, recall, F1—all perfect on test)
7. Built a simple Streamlit app for demo

**Best performers**: SVM and CNN both reached 100% accuracy.  

### 🛠️ Tech Stack
- Python 3
- Core libraries: pandas, numpy, scikit-learn, tensorflow/keras, hmmlearn, mlxtend, streamlit
- Developed in Jupyter Notebook (Colab-friendly)

### 📂 What's in the Repo

```
ML-Project/
├── ML_hackathon_PhishGuard.ipynb     # Full code, explanations, results
├── README.md                         # You're reading it!
└── (coming soon: app.py, requirements.txt, sample_data.csv)
```

---

### 🚀 How to Run It

#### 1️⃣ Clone the Repo

```bash
git clone https://github.com/sayed02-debug/ML-Project.git
cd ML-Project
```

---

#### 2️⃣ Install Dependencies

```bash
pip install pandas numpy scikit-learn tensorflow hmmlearn mlxtend streamlit
```

(Or use `requirements.txt` once added.)

---

#### 3️⃣ Open the Notebook

**Locally**
```
jupyter notebook ML_hackathon_PhishGuard.ipynb
```

**Or directly in Colab**
👉  [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/sayed02-debug/ML-Project/blob/main/ML_hackathon_PhishGuard.ipynb)


---


### 📈 Results at a Glance

The model achieved 100% accuracy on the current test dataset.  
(Note: The dataset size is limited, and performance will be further validated with larger real-world data.)

- Confusion Matrix: Clean perfect separation  
- Apriori found common phishing words like **"জরুরি", "পুরস্কার", "লিঙ্ক"** etc.

---

### ⚠️ Current Limitations & What's Next

- Dataset is still small → planning to collect more real examples  
- Add real-time API (e.g., integrate with Twilio for live SMS)  
- Mobile-friendly version  
- Try fine-tuned Bangla BERT for even better performance  

---

### 📄 Dataset

Custom Bangla SMS dataset, manually labeled.  
Full version linked in the notebook (Google Sheet).  
I'll add a sample CSV here soon.

---

### ❤️ Shoutouts

Built this for a Machine Learning hackathon.  
Huge thanks to open-source libraries and the community that makes projects like this possible.


## 📬 Let's Connect / Contribute

Md. Abu Sayed Islam  

LinkedIn: [linkedin.com/in/sayedo2](https://www.linkedin.com/in/sayedo2)  
Email: [mdabusayedislam2@gmail.com](mailto:mdabusayedislam2@gmail.com) 

Questions, ideas, collaborations? Drop me a message!  
Feel free to open issues or send PRs—happy to improve this together.  

If you like it, give the repo a star ⭐ — means a lot!

#BanglaAI #CyberSecurity #MachineLearning #PhishingDetection
