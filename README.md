# UniVerify

UniVerify is an open-source ML-powered microservice for automated verification of university student ID cards. It uses OCR and image classification to extract key information and verify document authenticity, streamlining student verification processes.

## Features

- OCR text extraction with Tesseract  
- Image classification using pretrained CNN models  
- Verification logic combining OCR and classification confidence  
- FastAPI backend API for easy integration  
- Privacy-focused: no image storage  

## Getting Started

### Prerequisites

- Python 3.8+  
- [Tesseract OCR](https://github.com/tesseract-ocr/tesseract) installed  

### Installation

```bash
git clone https://github.com/your-username/uni-verify.git
cd uni-verify
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
pip install -r requirements.txt
```

### Run the API

```bash
uvicorn app.main:app --reload
```

### Usage

- **POST** student ID images to the `/verify` endpoint  
- Receive extracted fields and verification status (`APPROVED` or `PENDING_MANUAL_REVIEW`)
