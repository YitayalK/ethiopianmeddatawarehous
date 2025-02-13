# ethiopianmeddatawarehous

This project is part of the **10 Academy: Artificial Intelligence Mastery** weekly challenge. The goal is to build a data warehouse for Ethiopian medical businesses by scraping data from Telegram channels, cleaning and transforming the data, performing object detection using YOLO, and exposing the data via a FastAPI application.

---

## Project Overview
The project involves the following tasks:
1. Data Scraping and Collection Pipeline: Scrape data from Telegram channels.
2. Data Cleaning and Transformation Pipeline: Clean and transform the scraped data.
3. Object Detection Using YOLO: Detect objects in images scraped from Telegram channels.
4. Data Warehouse Design and Implementation: Store and manage the data in a structured format.
5. Data Integration and Enrichment: Expose the data via a FastAPI application.

## Setup Instructions**

### **1. Clone the Repository**
```bash
git clone https://github.com/YitayalK/ethiopian-medical-data-warehouse.git
cd ethiopian-medical-data-warehouse
```

### **2. Set Up a Virtual Environment**
```bash
python -m venv venv
# On Windows: venv\Scripts\activate
```

### **3. Install Dependencies**
```bash
pip install -r requirements.txt
```

---
## **Running the Project**

### **1. Data Scraping**
- Run the Telegram scraper to collect data:
  ```bash
  python scripts/telegram_scraper.py
  ```
- Raw data will be stored in `data/raw/`.

### **2. Data Cleaning**
- Clean the scraped data:
  ```bash
  python scripts/data_cleaning.py
  ```
- Cleaned data will be stored in `data/cleaned/` and loaded into a SQLite database.

### **3. Object Detection**
- Detect objects in images using YOLO:
  ```bash
  python scripts/yolo_detection.py
  ```
- Detection results will be stored in a database table.

### **4. FastAPI Application**
- Start the FastAPI app to expose the data:
  ```bash
  uvicorn scripts.fastapi_app:app --reload
  ```
- Access the API at `http://127.0.0.1:8000`.

---

## **Tasks and Deliverables**

### **Task 1: Data Scraping and Collection Pipeline**
- Scrape data from Telegram channels using the `telethon` library.
- Store raw data in CSV files and a SQLite database.

### **Task 2: Data Cleaning and Transformation Pipeline**
- Clean the scraped data using `pandas`.
- Use DBT to transform and load data into the data warehouse.

### **Task 3: Object Detection Using YOLO**
- Detect objects in images using YOLOv5.
- Store detection results in a database.

### **Task 4: Data Warehouse Design and Implementation**
- Design a schema for storing scraped and cleaned data.
- Use DBT to create tables and perform transformations.

### **Task 5: Data Integration and Enrichment**
- Expose the data via a FastAPI application.
- Implement CRUD operations for querying and managing the data.

---

## **Dependencies**
- Python 3.8+
- Libraries: `telethon`, `pandas`, `sqlalchemy`, `dbt`, `opencv-python`, `torch`, `fastapi`, `uvicorn`

---
