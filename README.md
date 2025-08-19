# Face Detection

This project provides face detection in images and videos, cropping specific face regions (such as the eyes), and face censoring functionality.

---

## Features

🔍 **Face Detection**
- Detects faces in images and video frames.
- Using Dlib's `HOG` and OpenCV's `Haar Cascade` models

📸 **Image Scraping**
- Downloads face images automatically using SerpAPI (Google Images).
- Developing a robust and secure flow to download images (e.g., verifying secure connections). 

✂️ **Face Cropping**
- Crops the most upper-left face
- Crops face specific regions (e.g., eyes, mouth).

🔒 **Face Censoring**
- Censoring Faces in Videos

---

## Installation
1. **Clone the repository:** 
```bash
git clone https://github.com/Ali-Adel-Zewailcity/Face-Detection.git
cd Face-Detection
```

2. **Install the required packages:**
```bash
pip install -r requirements.txt
```

3. **Make sure you have a valid SerpAPI key for image crawling.<br>Update it in the code:**  
```bash
GoogleSearch.SERP_API_KEY = "your_api_key_here"
```
