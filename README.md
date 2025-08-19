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

---

## Project Flow
1. **Downloading Face Images**  
In the Project, The process of extracting images from the web is illustrated using `serpapi` to retrieve Images from `GoogleSearch`.
> The Images and Videos used in this project are already uploaded in `/Images` and there is no need to run that part of the project.

2. **Detecting and Cropping Faces**  
- Use `dlib’s face detector` to find faces and crop them.
- The model used is `dlib's HOG` model.
- A model like `CNN` is ignored because it is computationally heavy, requires a lot of resources and is time-consuming.
- Setting dlib detector **upsamlping ratio** to `1` as the speed is required since detecting very small faces is not a primary concern for this project.
- Cropping the most left-upper face in the image.

3. **Cropping Specific Regions (e.g., Eyes)**
- With `dlib’s 68 facial landmarks`, you can isolate regions like Eyes, Lips and Nose.

4. **Face Censoring in Video**
- Detecting Faces in Videos using OpenCV’s pre-trained `Haar Cascade` model to detect faces. 
- Censoring the detected face area and writing the result to a new video.
