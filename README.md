# 🌾 Rice Disease Detection Using DL& Soil Health Monitoring

## 📌 Overview  
This project integrates **Deep Learning (DL)** and **IoT-based soil monitoring** to support **precision agriculture**.  
It enables automated detection of rice leaf diseases using image classification models, along with **real-time soil health monitoring** (NPK, pH, temperature, and moisture).  

By combining **computer vision** with **IoT sensors**, the system helps farmers with:  
- Early detection of rice diseases  
- Real-time soil nutrient assessment  
- Data-driven recommendations for fertilizer & pesticide use  
- A web dashboard for monitoring and visualization  

---

## ✨ Features  
- ✅ **Rice Leaf Disease Detection** (10 classes, 97.5% accuracy)  
- ✅ **Soil Health Monitoring** using ESP32 + NPK, pH, DHT22 & moisture sensors  
- ✅ **Deep Learning Models**: EfficientNet-B4, DenseNet121, Xception, MobileNetV3, VGG19, InceptionV3  
- ✅ **Web Application** (Flask + Jinja) for real-time disease & soil reports  
- ✅ **Dashboard** with disease predictions, soil nutrient reports, and recommendations  
- ✅ **Hardware Integration** with IoT sensors and ESP32  

---

## 📂 Dataset  
- **Total Images**: 11,420 rice leaf images  
- **Classes (10)**:  
  - Bacterial Blight  
  - Brown Spot  
  - Leaf Smut  
  - Leaf Blast  
  - Tungro  
  - Sheath Blight  
  - Bacterial Leaf Streak  
  - Hispa  
  - Bacterial Panicle Blight  
  - Healthy Leaf  
- **Format**: JPEG, size 480×640 px  

---

## ⚙️ System Design  
### 🔹 Architecture  
- **Frontend**: Jinja web app (dashboard)  
- **Backend**: Flask REST API (model deployment + database)  
- **IoT Hardware**: ESP32 DevKit + Soil Sensors (NPK, pH, Moisture, DHT22)  
- **Outputs**:  
  - Disease type + confidence score  
  - Soil nutrient analysis & recommendations  

<p align="center">
  <img src="static/images/Hardware Setup.png" alt="Hardware Setup" width="800"/>
</p>
<p align="center">
  <sub>Figure 1: Hardware Setup</sub>
</p>

<p align="center">
  <img src="static/images/Full Project Setup.png" alt="Full Project Setup" width="800"/>
</p>
<p align="center">
  <sub>Figure 2: Full Project Setup</sub>
</p>


---

## 🧠 Deep Learning Workflow  
- **Data Preprocessing**: Augmentation (flip, rotate, crop, color jitter, Gaussian blur)  
- **Models**: Transfer Learning (EfficientNet, DenseNet, Xception, MobileNet, VGG19)  
- **Ensemble Model** achieved **97.5% accuracy, F1=0.98**  
- **Evaluation Metrics**: Accuracy, Precision, Recall, F1-Score, Confusion Matrix  

---

## 🔌 Hardware Setup  
- ESP32 DevKit V1  
- NPK Sensor (RS485)  
- Capacitive Soil Moisture Sensor  
- Soil pH Sensor  
- DHT22 (temperature & humidity)  
- Power Supply (18650 Li-ion + TP4056 charger)  

---

## 📊 Model Performance Comparison  

| Model                    | Accuracy (%) | F1 Score | Precision | Recall | Loss   | Std. Dev. |
|---------------------------|--------------|----------|-----------|--------|--------|-----------|
| EfficientNet-B4           | 97.13        | 0.97     | 0.97      | 0.97   | 0.1511 | 0.01      |
| Xception41                | 97.07        | 0.96     | 0.97      | 0.96   | 0.1406 | 0.02      |
| DenseNet121               | 97.20        | 0.98     | 0.99      | 0.97   | 0.1367 | 0.02      |
| DenseNet201               | 97.20        | 0.99     | 0.97      | 0.98   | 0.1312 | 0.02      |
| MobileNetV3-Large         | 96.73        | 0.96     | 0.96      | 0.96   | 0.1510 | 0.03      |
| InceptionV3               | 96.53        | 0.96     | 0.96      | 0.96   | 0.1487 | 0.03      |
| AlexNet                   | 95.60        | 0.95     | 0.95      | 0.95   | 0.2162 | 0.04      |
| ResNet50                  | 95.80        | 0.95     | 0.96      | 0.95   | 0.1566 | 0.02      |
| GoogLeNet / Inception-v1  | 97.07        | 0.97     | 0.97      | 0.97   | 0.1267 | 0.02      |
| VGG19                     | 93.87        | 0.94     | 0.94      | 0.94   | 0.2907 | 0.03      |
| ShuffleNet                | 92.13        | 0.92     | 0.92      | 0.92   | 0.2750 | 0.05      |
| SqueezeNet                | 89.73        | 0.90     | 0.90      | 0.90   | 0.3707 | 0.05      |
| Improved LeNet-5          | 86.67        | 0.87     | 0.87      | 0.87   | 0.6007 | 0.06      |
| **Ensemble Model**        | **97.50**    | **0.98** | **0.98**  | **0.98** | **0.5762** | **0.00** |

---

## 📽️ Project Demonstration  
Watch the full project demo video here:  

[![Rice Disease Detection Demo](https://img.youtube.com/vi/GOXaCI9eqBs/0.jpg)](https://www.youtube.com/watch?v=GOXaCI9eqBs)  

<sub>Click the thumbnail to watch on YouTube</sub>

---

## 💰 Cost Analysis  
Estimated project cost: **28,440 – 52,500 BDT**  
- Hardware (ESP32, sensors, batteries)  
- Cloud GPU access for model training  
- Deployment & maintenance  

---

## 🚀 Future Work  
- Develop a **mobile app** for field deployment  
- Integrate **drone-based imaging** for large-scale monitoring  
- Expand dataset for **better generalization**  
- Optimize for **lightweight edge devices**  

---



## 👨‍💻 Authors  
- **Chayon Kumar Das** 
- **Suvro Kumar Das** 
- Supervised by: **Md Toukir Ahmed**, Assistant Professor, Dept. of IoT & Robotics Engineering, University of Frontier Technology, Bangladesh 

---

## 📜 License  
This project is developed for **academic and research purposes**.  
Please cite the authors when using this work.
### 📥 Installation  
```bash
### 🚀 Getting Started

# Clone repository
git clone https://github.com/shuv001/Capstone-Project-RiceDiseaseDetectionSoilHealthMonitoring.git
cd Capstone-Project-RiceDiseaseDetectionSoilHealthMonitoring

# Install dependencies
pip install -r requirements.txt

# Run the web app
python app.py
