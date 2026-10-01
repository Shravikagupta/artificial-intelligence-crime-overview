# Artificial Intelligence Crime: An Overview of Malicious Use and Abuse of AI

B.Tech Final Year Project (Stage 2) — Computer Science Engineering (Data Science)
Swami Vivekananda Institute of Technology, Secunderabad (Affiliated to JNTU-H) | 2021–2025A 

Django web application that classifies AI-related cybercrime types (Social Engineering, Misinformation, Hacking, Autonomous Weapon Systems) from network/URL data using machine learning.

## 📌 Overview
AI is being increasingly misused for criminal activity such as deepfakes, AI-driven
phishing, social engineering, misinformation and autonomous attacks. This project
presents an overview of malicious use and abuse of AI and implements a web-based
system that predicts the **type of AI-related cybercrime** from network and URL
features using machine learning.

Malicious use categories covered:
- Social Engineering
- Misinformation / Fake News
- Hacking
- Autonomous Weapon Systems

Malicious abuse categories discussed: integrity attacks, unintended AI outcomes,
algorithmic trading, membership inference attacks.

## ✨ Features
- User registration and login
- Crime type prediction from input features (FID, URL, URL length, hostname length,
  source/destination IP and port)
- Admin (Service Provider) panel to:
  - Browse datasets and train/test models
  - View model accuracy as bar, line and pie charts
  - View predicted crime types and crime type ratios
  - Download predicted datasets as Excel
  - View and manage registered remote users

## 🧠 Machine Learning Models
| Model | Accuracy |
|---|---|
| Naive Bayes | 38.19% |
| Extra Tree Classifier | 35.48% |
| Decision Tree Classifier | 36.55% |
| SVM (LinearSVC) | 38.01% |
| Logistic Regression | 39.15% |

Text features are extracted from URLs using `CountVectorizer`. The dataset is split
80/20 for training and testing.

## 🛠️ Tech Stack
- **Language:** Python
- **Backend:** Django
- **ML:** scikit-learn, pandas, NumPy
- **Visualization:** Matplotlib, chart templates
- **Database:** MySQL
- **Other:** xlwt (Excel export)

## 💻 System Requirements
- Windows 8 or above
- Intel i3 or above, 4 GB RAM, 40 GB disk
- Python 3.x, MySQL

## 🚀 Installation & Setup
```bash
# 1. Clone the repository
git clone https://github.com/<your-username>/ai-crime-detection.git
cd ai-crime-detection

# 2. Create a virtual environment
python -m venv venv
venv\Scripts\activate        # Windows

# 3. Install dependencies
pip install -r requirements.txt

# 4. Create the MySQL database
#    CREATE DATABASE artificial_intelligence_crime;
#    Update credentials in settings.py (use environment variables, don't commit passwords)

# 5. Apply migrations
python manage.py makemigrations
python manage.py migrate

# 6. Run the server
python manage.py runserver
```
Open `http://127.0.0.1:8000/` in your browser.

## 📂 Project Structure
artificial_intelligence_crime/ # Django project settings & URLs
Remote_User/ # User registration, login, prediction
Service_Provider/ # Admin: training, charts, ratios, downloads
Template/ # HTML templates, images, media
Datasets.csv # Training dataset
manage.py
