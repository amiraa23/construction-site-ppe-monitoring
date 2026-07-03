# Construction Site PPE Monitoring

A computer vision system for detecting personal protective equipment (PPE) compliance in construction-site videos using YOLOv8.

The system detects safety-related classes such as helmets, vests, gloves, boots, goggles, persons, and missing PPE violations. It supports video-based monitoring, model comparison, compliance analysis, and interactive deployment through Hugging Face / Streamlit.

---

## Overview

Construction sites require continuous safety monitoring to reduce accidents and enforce PPE compliance. Manual monitoring can be inconsistent, time-consuming, and difficult to scale.

This project uses YOLOv8 object detection to identify whether workers are wearing required PPE items and to detect missing safety equipment in construction-site images and videos.

The project includes:

- YOLOv8 model training
- Model comparison
- Video inference
- PPE compliance analysis
- Safety-event reporting
- Hugging Face / Streamlit interactive demo

---

## Demo

Watch the project demo video here:

[Watch Demo Video on Google Drive](PASTE_GOOGLE_DRIVE_DEMO_LINK_HERE)

Hugging Face Demo:

[Open Hugging Face Space](PASTE_HUGGING_FACE_LINK_HERE)

---

## Key Features

- PPE detection using YOLOv8
- Image and video inference
- Detection of safety equipment and missing PPE violations
- Model comparison between YOLOv8n, YOLOv8s, and YOLOv8m
- Compliance analysis and safety-event reporting
- Model export for deployment flexibility
- Interactive demo through Hugging Face / Streamlit

---

## Detected Classes

The model detects PPE-related classes including:

- Person
- Helmet
- Vest
- Gloves
- Boots
- Goggles
- No Helmet
- No Gloves
- No Boots
- No Goggles

---

## Tech Stack

| Area | Tools |
|---|---|
| Object Detection | YOLOv8 / Ultralytics |
| Computer Vision | OpenCV |
| Video Processing | OpenCV, supervision |
| Data Analysis | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| Deployment | Streamlit, Hugging Face |
| Notebook Environment | Jupyter / Google Colab |

---

## Model Training and Comparison

Three YOLOv8 models were trained and compared:

| Model | Purpose |
|---|---|
| YOLOv8n | Fastest model for real-time or edge use cases |
| YOLOv8s | Best overall balance between speed and detection quality |
| YOLOv8m | Larger model tested for comparison |

YOLOv8s was selected as the best overall model based on final evaluation results, while YOLOv8n provided the fastest inference speed.

---

## Results Summary

| Model | Precision | Recall | mAP50 | mAP50-95 |
|---|---:|---:|---:|---:|
| YOLOv8s | 0.788 | 0.395 | 0.432 | 0.277 |

The results show that the system can detect PPE-related objects and safety violations, while also highlighting practical limitations such as class imbalance, small-object detection challenges, occlusion, and difficult visual conditions in construction-site scenes.

---
## Project Structure

```text
construction-site-ppe-monitoring/
│
├── notebooks/
│   └── Amira_Elsayed_ConstructionSiteMonitoring.ipynb
│
├── assets/
│   ├── screenshots/
│   └── metrics/
│       ├── map50_comparison.png
│       ├── map5095_comparison.png
│       ├── precision_recall_comparison.png
│       ├── confusion_matrix_yolov8s.png
│       ├── pr_curve_yolov8s.png
│       └── f1_curve_yolov8s.png
│
│
├── README.md


---

## How to Run

### 1. Install requirements

```bash
pip install -r requirements.txt
```

### 2. Open the notebook

```bash
jupyter notebook
```

Then open:

```text
notebooks/Amira_Elsayed_ConstructionSiteMonitoring.ipynb
```

### 3. Run the notebook cells

The notebook includes:

- Dataset loading
- YOLOv8 training configuration
- Model training
- Model evaluation
- Model comparison
- Video inference
- PPE compliance analysis
- Streamlit demo setup

---

## Deployment

The project includes an interactive Hugging Face / Streamlit demo where users can upload construction-site videos and run PPE detection.

Hugging Face Space:

[Open Hugging Face Space](https://www.google.com/url?q=https%3A%2F%2Fhuggingface.co%2Fspaces%2FAmira222%2Fconstruction-safety-monitoring)

---

## Demo Video

The demo video shows:

1. Opening the deployed interface
2. Uploading a construction-site video
3. Running YOLOv8 PPE detection
4. Detecting workers and safety equipment
5. Identifying missing PPE violations
6. Displaying detection results and compliance output

Demo link:

[Watch Demo Video on Google Drive](https://drive.google.com/file/d/1aiDLHdXcAqQuxlFe59jJQzxvfGCsgdLg/view?usp=drivesdk)

---

## Limitations

This project is an applied computer vision prototype and has some limitations:

- The model may struggle with small or partially occluded PPE items.
- Recall is lower than precision, meaning some PPE violations may be missed.
- Performance depends on lighting, camera angle, video quality, and object size.
- The current version is not a certified industrial safety system.
- Further improvement would require more diverse real-world construction-site data.

---

## Future Improvements

Possible future improvements include:

- Add more construction-site video data
- Improve detection of small PPE items
- Fine-tune class balancing
- Add real-time webcam support
- Add alert notifications for safety violations
- Deploy optimized ONNX model for faster inference
- Build a dashboard for daily compliance reports
- Add worker-level PPE compliance tracking

---

## What I Learned

Through this project, I practiced:

- Training YOLOv8 object detection models
- Comparing object detection model variants
- Evaluating detection performance using mAP metrics
- Running inference on construction-site videos
- Building video-based safety monitoring workflows
- Deploying an interactive AI demo using Streamlit and Hugging Face
- Understanding trade-offs between speed, accuracy, and deployment constraints

---

## Conclusion

Construction Site PPE Monitoring demonstrates how computer vision can support workplace safety by detecting PPE usage and missing safety equipment in construction-site videos.

The project combines YOLOv8 training, model comparison, video inference, compliance analysis, and deployment to create a practical AI safety-monitoring prototype.
