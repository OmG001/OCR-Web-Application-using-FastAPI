# 🖼️ OCR Web Application Using FastAPI

A simple and efficient **Optical Character Recognition (OCR)** web application built with **FastAPI** that extracts text from images. The application supports both **single-image OCR** and **bulk-image OCR**, offering results via a clean web interface and RESTful APIs.

---

## 📌 Overview

This project allows users to upload image files containing text and converts them into **machine-readable text** using **Tesseract OCR**.
It is lightweight, easy to use, and ideal for **learning, demos, and portfolio projects**.

---

## 🎯 Use Cases

* Extract text from scanned documents
* Convert printed text images into editable text
* Process multiple images at once (bulk OCR)
* Learn how OCR integrates with FastAPI
* Demonstrate asynchronous background processing in APIs

---

## ✨ Features

* Upload and extract text from a **single image**
* **Bulk OCR** support for multiple images
* Background processing for bulk uploads
* RESTful API architecture
* Simple and responsive web UI
* Automatic `.txt` file generation for bulk OCR results

---

## 🛠 Tech Stack

### Backend

* **Python**
  Main programming language; well-suited for OCR and backend services

* **FastAPI**

  * Builds REST APIs
  * High performance and lightweight
  * Automatic request validation
  * Native support for async programming

* **Uvicorn**

  * ASGI server for running FastAPI
  * High-performance and async-friendly

* **Pytesseract**

  * Python wrapper for Google’s Tesseract OCR engine
  * Converts image content into text

* **Pillow (PIL)**

  * Image processing library
  * Required by pytesseract for handling images

* **Python-Multipart**

  * Handles file uploads in FastAPI

---

### Frontend

* **HTML** – UI structure
* **Bootstrap** – Responsive styling without custom CSS
* **jQuery** – AJAX requests and dynamic file uploads
* **SweetAlert** – Clean popup display for extracted text

---

### Environment & Dependency Management

* **Virtual Environment (venv)**

  * Isolates project dependencies
  * Prevents version conflicts

* **requirements.txt**

  * Lists all required Python packages
  * Simplifies project setup

---

## 📂 Project Structure

```bash
.
├── main.py               # FastAPI app and API routes
├── ocr.py                # OCR processing logic
├── index.html            # Frontend interface
├── requirements.txt      # Python dependencies
├── package-lock.json     # Node metadata (minimal usage)
├── venv/                 # Virtual environment
├── temp/                 # Temporary file storage
└── templates/            # HTML templates
```

---

## 🔌 API Endpoints

### 🏠 Home Page

```http
GET /
```

Loads the web interface.

---

### 🖼️ Single Image OCR

```http
POST /api/v1/extract_text
```

* Accepts one image file
* Returns extracted text as JSON

---

### 📂 Bulk Image OCR

```http
POST /api/v1/bulk_extract_text
```

* Accepts multiple image files
* Runs OCR in the background
* Returns a task ID

---

### 📄 Fetch Bulk OCR Results

```http
GET /api/v1/bulk_output/{task_id}
```

* Returns extracted text for each uploaded image

---

## 🚀 Getting Started

### ✅ Prerequisites

* Python **3.8+**
* **Tesseract OCR** installed on your system

---

### 📥 Installation

#### 1️⃣ Clone the Repository

```bash
git clone <repository-url>
cd <project-folder>
```

#### 2️⃣ Create & Activate Virtual Environment

```bash
python -m venv venv
```

**macOS / Linux**

```bash
source venv/bin/activate
```

**Windows**

```bash
venv\Scripts\activate
```

#### 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

#### 4️⃣ Install Tesseract OCR

* **Windows**: Download and install from the official Tesseract installer
* **Linux/macOS**: Install via package manager (apt, brew, etc.)

---

## ▶️ Run the Application

```bash
uvicorn main:app --reload
```

Open your browser and visit:

```
http://127.0.0.1:8000
```

---

## 🧪 How to Use

1. Open the application in your browser
2. Select one or more image files
3. Click **Extract Text**
4. View extracted text in popup alerts
5. For bulk uploads, results appear automatically as buttons

---

## 📈 Future Enhancements

* Multi-language OCR support
* Download extracted text files
* Authentication & user accounts
* Improved UI using React or Vue
* Docker containerization
* Database storage for OCR results

---

## 📄 License

This project is **open-source** and free to use for **educational and personal purposes**.

---
