# 🧾 CheckSmart: Cheque Image Feature Extraction System

**Authors:** Shivanshu Mishra , Amrit Pandey 

---

## 📌 Overview

CheckSmart is a cheque processing system built to extract key fields from Indian cheque images using OCR and deep learning. It supports both individual and batch image processing and outputs structured information in **CSV** or **JSON** format.

**Extracted Fields:**
- Payee Name
- Date
- Amount in Digits
- Amount in Words

> ⚙️ The system uses manual cropping + field-specific OCR models (based on TrOCR) for higher accuracy on handwritten cheques.

---

## 🧠 Core Technologies

- Python & PyTorch
- HuggingFace Transformers
- TrOCR (Transformer-based OCR by Microsoft)
- Google Cloud Platform (GCP)
- TorchVision for Augmentation

---

## 📂 Project Structure


---

## 🔍 How It Works

1. **Image Preprocessing** – Resize, crop, and mask cheque images.
2. **Manual Labeling** – Labels stored in JSON for each field.
3. **Field-Specific Model Training** – Each field is trained using `microsoft/trocr-base-handwritten`.
4. **Inference & Output** – Outputs structured data in `.csv` or `.json`.

---

## 🔒 Note on Cheque Images and Model Access

Due to restrictions from the bank, we are **unable to share cheque image data** publicly.

However, we have shared the **trained model** — the link can be found in the [`model_link.txt`](https://github.com/shivanshu2109/CheckSmart/blob/main/model_link.txt) file in this repository.

We are actively working on improving this model and will continue to update the shared link as we develop better versions tailored to various fields.

**Stay tuned and keep coding! 🚀**

---

## 📊 Model Performance

| Field              | Training Accuracy | Validation Accuracy | Notes                            |
|-------------------|-------------------|---------------------|----------------------------------|
| Payee             | 98.82%            | 52.28%              | Overfitting due to label skew    |
| Date              | 68.85%            | 64.77%              | Format inconsistencies           |
| Amount in Digits  | 99.06%            | 91.09%              | Most reliable field            |
| Amount in Words   | 88.60%            | 49.78%              | Hardest field due to variation   |

---

## 🧪 Evaluation Metric

- Metric Used: **Exact Match Accuracy**
- Model: `microsoft/trocr-base-handwritten`
- Evaluation: Based on field-wise text match (case & whitespace insensitive)

---


## 📬 Contact

For queries or suggestions, feel free to reach out to:
- Shivanshu Mishra - shivanshu985@gmail.com
- Amrit Pandey - amritsga123@gmail.com

---

> 💡 This project showcases how OCR and domain-specific preprocessing can work together to tackle real-world handwritten document digitization. Thanks for visiting!


