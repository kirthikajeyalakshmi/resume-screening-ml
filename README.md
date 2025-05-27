# 🤖 Resume Screening ML-Based System

A machine learning–powered web application that automates the process of screening resumes. It enables recruiters and HR professionals to upload resumes and receive:

- Predicted job domain classification  
- Relevant job role suggestions  
- Extracted contact details, skills, and education information  

## 📘 Introduction

Recruitment today is becoming smarter with the help of machine learning. This project showcases an end-to-end system that simplifies the process of resume screening. It can predict the job category of a candidate, suggest relevant job roles, and extract important information from resumes automatically.

## 🧹 The Challenge

Hiring teams often have to manually go through hundreds of resumes, which takes time and can be inconsistent. It’s difficult to extract details like skills and education quickly, and there’s always a chance of human error. Automating this can help save time, reduce mistakes, and make the hiring process more efficient.

## 💡 Proposed Solution

This project implements a complete resume screening pipeline, capable of:

- **Resume Upload:** Accepts files in PDF format  
- **Text Extraction:** Extracts raw text using PyPDF2  
- **Data Preprocessing:** Cleans extracted text (removes punctuation, stopwords, etc.)  
- **Resume Categorization:** Predicts the resume's domain using a trained ML model  
- **Job Role Recommendation:** Suggests roles based on categorized domain and keywords  
- **Information Extraction:** Pulls out:  
  - Name  
  - Phone Number  
  - Email  
  - Skills  
  - Educational background  

## 🧪 Model Training Summary

✅ **Resume Categorization Model**  
- Algorithm: Random Forest Classifier  
- Feature Extraction: TF-IDF Vectorizer  
- Training Accuracy: 84.2%  
- Dataset: Public dataset of resumes labeled by domain  

*Note:* The model performs well generally, but may occasionally misclassify due to limitations in data variety and resume formats.

⚠️ **Job Role Recommendation Logic**

- A dedicated, labeled dataset for job role prediction was not available  
- A small synthetic dataset was created for basic recommendations  
- Accuracy: ~10% (due to minimal data and simple keyword-based logic)  
- Suggests 1–2 roles based on the domain and extracted keywords  

*Note:* As a placeholder logic, it functions reasonably but may return inconsistent or inaccurate results depending on input text.

## 🔄 System Workflow

| Step Description                          |
|------------------------------------------|
| Upload Resume (PDF)                       |
| Text Extraction using PyPDF2             |
| TF-IDF Vectorization and ML Prediction   |
| Resume Categorization                     |
| Job Role Recommendation Logic            |
| Extract Name, Email, Phone, Skills, etc. |
| Display Output on Web Interface           |


## 🛠️ Tech Stack

### 🔗 Backend:

- Python 3.10  
- Flask – Web framework for building the web application  
- PyPDF2 – For extracting text from PDF resumes  
- Regex – Used for extracting email addresses, phone numbers, etc.  
- Scikit-learn – Machine learning library used for TF-IDF and Random Forest  
- Pickle – For saving and loading trained ML models  

### 🎨 Frontend:

- HTML/CSS – Structure and styling of web pages  
- Jinja2 – Flask's templating engine for dynamic HTML rendering  

## 🎯 Features

- ✅ Resume Upload  
  Upload resumes via a web interface (.pdf format supported)  

- ✅ Resume Text Extraction  
  Automatically reads and extracts raw text from uploaded files  

- ✅ Resume Categorization  
  Predicts the job domain of the candidate's resume using ML  

- ✅ Job Role Recommendation  
  Suggests 1–2 relevant roles based on text and domain  

- ✅ Resume Parsing  
  Extracts structured information such as:  
  - Name (or fallback to file name)  
  - Phone number  
  - Email address  
  - Technical skills (from predefined set)  
  - Education (detected from degree-related keywords)  

- ✅ Web Interface Output  
  Clean and readable results displayed in the browser  

## 🚧 Limitations
- Job recommendation model is based on limited data and simple rules
- Resume categorization may fail or mislabel resumes outside of training distribution
- Extraction accuracy can vary depending on resume formatting
- Name detection may be imprecise if the resume format is non-standard


