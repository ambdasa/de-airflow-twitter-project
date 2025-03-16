# **📌 Twitter Data Pipeline Using Apache Airflow & AWS**  

## **🚀 Overview**  
This project builds an **automated data pipeline** that extracts **real-time tweets**, processes them using **Python**, orchestrates the workflow using **Apache Airflow**, and stores the data in **Amazon S3** for further analysis.  

![image](https://github.com/user-attachments/assets/db427031-2031-4a7a-b3eb-abac7cd3da4f)

📌 **Workflow Breakdown:**  
1️⃣ **Extract tweets** from **Twitter API** using **Python**.  
2️⃣ **Process & clean data** before storage.  
3️⃣ **Use Apache Airflow (hosted on EC2)** to schedule and automate the pipeline.  
4️⃣ **Store structured tweets in Amazon S3** for further processing or analytics.  

---

## **🛠 Tech Stack**  
- **Programming Language**: Python  
- **Orchestration**: Apache Airflow (on AWS EC2)  
- **Cloud Storage**: Amazon S3  
- **API Integration**: Twitter API  

---

## **📂 Project Structure**  
```
├── dags/                    # Airflow DAGs (Workflow Definitions)
│   ├── twitter_pipeline.py  # DAG for fetching and storing tweets
│   ├── config.py            # API keys and configuration
├── scripts/                 # Python scripts for API extraction
│   ├── fetch_tweets.py      # Extracts tweets from Twitter API
│   ├── process_tweets.py    # Data cleaning and preprocessing
├── requirements.txt         # Dependencies for Python & Airflow
├── README.md                # Project documentation
└── config/                  # Configuration files
```

---

## **📌 Workflow Explained**  
### **1️⃣ Data Extraction**  
- The **Twitter API** is used to fetch live tweets based on specific keywords, hashtags, or user handles.  

### **2️⃣ Data Processing**  
- The extracted tweet data is **cleaned** and formatted (removing special characters, filtering retweets, etc.).  

### **3️⃣ Workflow Automation with Apache Airflow**  
- Apache Airflow (hosted on **AWS EC2**) schedules and manages the end-to-end pipeline.  
- Airflow ensures the pipeline runs **automatically at scheduled intervals** or **on demand**.  

### **4️⃣ Storing Data in Amazon S3**  
- The **processed tweets** are saved in **Amazon S3** in JSON/CSV format for further analysis.  
- S3 enables **cost-effective** and **scalable storage** for large tweet datasets.  

---

## **🚀 Setting Up the Project**  
### **1️⃣ Prerequisites**  
✔ AWS Account (for **EC2 & S3**)  
✔ Twitter Developer Account (for **API keys**)  
✔ Python 3.x installed  
✔ Apache Airflow setup on EC2  

### **2️⃣ Steps to Deploy**  
1. **Create an S3 bucket** to store the tweets.  
2. **Launch an EC2 instance** and install Apache Airflow.  
3. **Configure the Twitter API keys** in the project.  
4. **Deploy Airflow DAGs** to automate the pipeline.  

---

## **📌 Use Cases**  
✅ **Social Media Analytics** – Analyze trends, hashtags, and user sentiment.  
✅ **Real-Time Monitoring** – Track breaking news, public sentiment, and trending topics.  
✅ **Data Storage & Future Processing** – Store tweets for later analysis using **AWS Glue, Athena, or Redshift**.  

---

## **⚡ Challenges & Solutions**  
🔹 **Twitter API Rate Limits** → Implemented **pagination & sleep intervals** between API calls.  
🔹 **Handling Large Tweet Volumes** → Used **batch processing** before writing to S3.  
🔹 **Ensuring Airflow Reliability** → Set up **retry policies** and logging for debugging failures.  

---
