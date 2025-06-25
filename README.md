# 🔗 Hybrid File System

A hybrid file system combining local disk operations, cloud storage (Google Drive), and metadata management (SQLite). It allows users to create, manage, view, and sync files across local storage and cloud with a simple web interface.

---

## 📌 Features

✅ Create and read text files  
✅ Maintain file structure using JSON  
✅ Track file metadata using SQLite (name, size, path, modified time)  
✅ Upload files to Google Drive  
✅ Restore/download/delete files from Google Drive  
✅ View local metadata and cloud files  
✅ Flask-powered GUI with multiple routes for user interaction

---

## 🗂️ Project Structure

Hybrid_File_System/
│
├── app.py # Main Flask app
├── requirements.txt # Python dependencies
├── Procfile # Deployment entry for gunicorn
├── schema.sql # SQLite schema
│
├── metadata/
│ ├── db.py # SQLite DB functions (init, fetch, upsert)
│
├── cloud/
│ ├── gdrive_backup.py # Google Drive upload/download integration
│
├── static/
│ └── style.css # Stylesheet (optional)
│
├── templates/
│ ├── index.html # Homepage
│ ├── local.html # Local operations UI
│ ├── cloud.html # Cloud operations UI
│ └── metadata.html # Metadata viewer
│
├── main3.py # Core logic for file creation, writing, deletion
├── check_metadata.py # Utility to fetch metadata via DB
└── filesystem.json # Stores the virtual structure of the file system

---

## ⚙️ Installation

### ✅ Prerequisites

- Python 3.9+
- Git
- Google Cloud OAuth 2.0 credentials JSON (named `credentials.json`)

---

### 🧪 Steps to Run Locally

```bash
# 1. Install dependencies
pip install -r requirements.txt

# 2. Initialize the database
python init_db

# 3. Run the Flask server
python app.py

## 🔗 Live Deployment

Access the Hybrid File System Web App here:  
👉 [hybrid-file-system.onrender.com](https://hybrid-file-system.onrender.com)
