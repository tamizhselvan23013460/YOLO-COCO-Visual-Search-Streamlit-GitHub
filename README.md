# YOLOv11 Image Search App

### NAME : TAMIZHSELVAN B
### REG.NO : 212223230225
A powerful **computer-vision powered search engine** built using **YOLOv11** and **Streamlit**.  
This tool lets you **run object detection**, **generate metadata**, and **search images based on objects, counts, and logical conditions**.

---

## Features

- Process a folder of images using **YOLOv11**
- Automatically generate **detection metadata (JSON)**
- Load existing metadata anytime
- Search using:
  - Selected object classes  
  - Class count thresholds  
  - AND / OR logic  
- Clean grid-view display of results
- Bounding box overlays
- Highlight matched objects
- Download search results (JSON)
- Beautiful UI with custom CSS

---

## Project Structure

```
Yolov11_Image_search/
│
├── app.py # Main Streamlit application
├── requirements.txt # Python dependencies
│
├── src/
│ ├── inference.py # YOLOv11 inference logic
│ ├── utils.py # Metadata utilities & helpers
│
├── models/
│ └── yolo11m.pt # YOLOv11 model weights
│
├── images/ # Image dataset directory
│
└── metadata/
└── detections.json # Auto-generated metadata (optional)
```
---
### Requirements:
```
streamlit
pillow
ultralytics
opencv-python
numpy
```
## Installation

###  Clone the Repository
```bash
git clone https://github.com/<your-username>/Yolov11_Image_search.git
cd Yolov11_Image_search
```
### Create Virtual Environment
```bash
python -m venv venv
source venv/bin/activate   # Linux/Mac
venv\Scripts\activate      # Windows
```
### Install Dependencies
```bash
pip install -r requirements.txt
```
## Running the Application
### Default Port (8501)
```bash
streamlit run app.py
```
### Custom Port (8080)
```bash
streamlit run app.py --server.port 8080
```

## How It Works

### Process New Images
- Provide image directory  
- Provide YOLOv11 model path  
- Run inference  
- Metadata JSON is generated  
- App automatically extracts:
  - Unique classes  
  - Count of each class per image  

---

### Load Existing Metadata
- Provide metadata JSON path  
- App reads detections + class counts  
- Ready for searching instantly  

---

### Smart Search Options
You can search for images that contain:

- **Any** of selected classes (OR mode)  
- **All** selected classes (AND mode)  
- **Count thresholds** for each class  

#### Example:
> Show images with **person ≤ 3 AND car ≤ 1**

## Exporting Results

### Download:
```
search_results.json
```

## Metadata Format Example

```json
{
  "image_path": "images/img1.jpg",
  "detections": [
    {
      "class": "person",
      "confidence": 0.92,
      "bbox": [120, 45, 260, 300]
    }
  ],
  "class_counts": {
    "person": 2,
    "car": 1
  }
}
```

## OUTPUT :
<img width="1920" height="1079" alt="image" src="https://github.com/user-attachments/assets/3c2257cf-c17f-4b06-9b06-c53c1ceaba7b" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/f9161f7d-a947-4691-8636-4038a242bb10" />
<img width="1915" height="1063" alt="image" src="https://github.com/user-attachments/assets/5e49e8cc-4079-4450-ad12-0f51d09043c9" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/d07ca6cb-2b34-4271-9659-8f04772e84d9" />



## RESULT:
Thus, the YOLOv11 Image Search App is implemented and successfully executed.
