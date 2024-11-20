# DistilBERT Intent Detection Fine-Tuning Project

This repository contains a project where I fine-tuned a pretrained **DistilBERT** model for intent detection in conversational messages. The project guides you through the end-to-end process of training and fine-tuning the model, from data preparation to model deployment.

---

## 📑 **Table of Contents**
1. Introduction  
2. Data Loading and Preprocessing  
3. Encoding Intent Features  
4. Tokenization  
5. Fine-Tuning the DistilBERT Model  
6. Evaluation  
7. Saving, Loading, and Inference  

---

## 🛠 **Getting Started**
### Prerequisites
- Python 3.8 or later
- Required libraries: `transformers`, `torch`, `pandas`, `scikit-learn`, `matplotlib`

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/HelpRam/Fine-Tune-Pretrained-model-DistilBert-.git
   ```
2. Install the required libraries:
   ```bash
   pip install -r requirements.txt
   ```

---

## 🚀 **Project Workflow**

### **1. Data Loading and Preprocessing**
- The dataset contains conversational messages and corresponding intent labels. 
- The preprocessing step cleans the data and prepares it for tokenization.

### **2. Encoding Intent Features**
- Intent labels are transformed into a format suitable for training (e.g., integers).

### **3. Tokenization**
- The `DistilBertTokenizer` is used to tokenize and encode the input text into `input_ids` and `attention_mask`.

### **4. Fine-Tuning**
- The `DistilBertForSequenceClassification` model is fine-tuned on the intent detection dataset.

### **5. Evaluation**
- The model's performance is evaluated using metrics such as precision, recall, F1-score, and a confusion matrix. 
- The results indicate robust intent detection capabilities.

### **6. Saving and Inference**
- The trained model is saved for reuse.
- Inference scripts demonstrate how to load the model and predict intents for new messages.

---

## 📊 **Dataset**
The dataset consists of labeled conversational messages. Labels represent intents such as:
- Question
- Statement
- Greeting  
...and more.

---

## 🧪 **Model Details**
- **Model**: Pretrained DistilBERT (Hugging Face)
- **Fine-Tuning**: Adapted for sequence classification with intent labels.

---

## 💡 **Results**
- The fine-tuned DistilBERT model achieves high accuracy on the test set. Detailed metrics and performance evaluations are available in the report.

---

## 🚀 **How to Use**
1. Train your own model or use the provided fine-tuned model.
2. Run inference to detect intents for conversational messages:
   ```python
   from transformers import pipeline
   
   classifier = pipeline("text-classification", model="path/to/your/model")
   result = classifier("What's the weather like today?")
   print(result)
   ```
---

## 📝 **License**
This project is licensed under the MIT License. See the LICENSE file for details.

---

### 🙌 **Acknowledgements**
- Hugging Face for the DistilBERT model
- Open-source datasets used for intent detection tasks

Contributions are welcome! 😊
