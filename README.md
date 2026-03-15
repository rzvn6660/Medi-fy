
# Medi-Fy – Medicine Information Chatbot

## Overview

Medi-Fy is an AI-based chatbot system that extracts and provides important information from medicine labels. The system uses Optical Character Recognition (OCR) and Natural Language Processing (NLP) to read text from medicine label images and provide structured information such as medicine name, dosage, usage instructions, and side effects.

The objective of this project is to make medicine information easily accessible to users, especially elderly individuals and visually impaired people who may have difficulty reading printed medicine labels. The system provides a simple interface where users can upload an image of a medicine label and quickly obtain relevant information.

This project was developed as part of a Bachelor of Technology program in Artificial Intelligence and Data Science. 

---

## Features

* Upload medicine label images for analysis
* Extract text using Pytesseract OCR
* Image preprocessing for better text detection
* Display medicine usage, dosage, and side effects
* Integration with OpenFDA database for additional medicine information
* Local dataset fallback when API data is unavailable
* Simple and interactive user interface built with Gradio

---

## System Workflow

1. User uploads an image of a medicine label.
2. Image preprocessing improves clarity using grayscale conversion and noise reduction.
3. OCR extracts text from the processed image.
4. Extracted text is cleaned and filtered using NLP techniques.
5. The system retrieves medicine information from OpenFDA or a local dataset.
6. Results are displayed through the Gradio interface.

---

## Technologies Used

| Technology     | Purpose                        |
| -------------- | ------------------------------ |
| Python         | Core programming language      |
| OpenCV         | Image preprocessing            |
| PIL (Pillow)   | Image processing               |
| Pytesseract    | Optical Character Recognition  |
| NLP Techniques | Text cleaning and processing   |
| Gradio         | User interface                 |
| OpenFDA API    | Medicine information retrieval |

---

## System Architecture

The system consists of three main layers:

### User Interface Layer

Provides a Gradio interface that allows users to upload medicine label images or enter medicine names.

### Backend Processing Layer

Handles image preprocessing, text extraction using Tesseract OCR, and NLP-based text cleaning.

### Data Retrieval Layer

Retrieves medicine information from the OpenFDA database. If data is not available online, the system uses a locally stored medicine dataset.

---

## Installation

### Clone the repository

```
git clone https://github.com/rzvnn6660/medify.git
cd medify
```

### Install required dependencies

```
pip install pytesseract
pip install opencv-python
pip install pillow
pip install gradio
pip install requests
```

### Install Tesseract OCR

Download and install Tesseract OCR from:

[https://github.com/UB-Mannheim/tesseract/wiki](https://github.com/UB-Mannheim/tesseract/wiki)

After installation, configure the path in Python if required:

```
pytesseract.pytesseract.tesseract_cmd = r'C:\Program Files\Tesseract-OCR\tesseract.exe'
```

---

## Running the Project

Run the main application:

```
python app.py
```

After running the script, a Gradio interface link will appear in the terminal. Open the link in a browser to use the application.

---

## Project Structure

```
medify/
│
├── app.py
├── preprocessing.py
├── ocr_extraction.py
├── medicine_data.json
├── requirements.txt
└── README.md
```

---

## Applications

The system can be used in various healthcare and digital applications including:

* Healthcare systems for quick medicine information access
* Pharmacy management systems
* Patient assistance tools
* Telemedicine and online consultations
* Digital health platforms
* Medical research data collection

---

## Advantages

* Improves accessibility of medicine information
* Reduces human error when reading labels
* Saves time compared to manual interpretation
* Provides a user-friendly interface
* Uses OCR techniques for automated information extraction

---

## Limitations

* OCR accuracy depends on image quality
* Blurry images or poor lighting may reduce accuracy
* Different label formats may affect extraction performance

---

## Future Scope

Possible improvements include:

* Development of Android and iOS mobile applications
* Support for multiple languages
* Integration with advanced OCR models such as CRNN or transformer-based models
* Real-time processing using mobile camera input
* Voice-based medicine information assistance

---
