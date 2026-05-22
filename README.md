#  Automated Animal Intrusion Detection and Repellent Activation

##  Project Overview
This project presents an **edge AI–based vision system** to protect agricultural fields from animal intrusion. Using **YOLOv8 and YOLOv11** models deployed on a **Raspberry Pi 4**, the system detects monkeys, elephants, and wild boars in real time. Once detected, deterrent mechanisms (speaker, spray, alarms) are activated automatically, and farmers are notified via GSM SMS alerts.

The framework integrates sensors, computer vision, and intelligent decision-making to provide a reliable, cost-effective solution for crop protection.

---

##  Objectives
- Provide real-time monitoring of crop fields  
- Detect animal intrusion using deep learning models (YOLOv8, YOLOv11)  
- Automate deterrent activation without human intervention  
- Notify farmers instantly via GSM alerts  
- Demonstrate edge AI deployment on Raspberry Pi for agriculture  

---

##  Detection Strategy
The system uses a hybrid detection approach:

- **IR Motion Sensor** → Activates Raspberry Pi and camera only when movement is detected, saving power.  
- **YOLO Classifier (v8 & v11)** → Processes captured frames, draws bounding boxes, and classifies animals with confidence scores.  
- **Decision Logic** → Selectively activates deterrents:
  - Loudspeaker/alarms for elephants  
  - Repellent sprays for monkeys  
  - Alarms for wild boars  

---

##  System Architecture
- IR Motion Sensor detects movement  
- Raspberry Pi + Pi Camera captures frames and runs YOLO inference  
- GSM Module sends SMS alerts to farmers  
- GPIO Circuits control deterrent devices (speaker, spray, alarms)  

This ensures continuous monitoring, accurate detection, rapid response, and farmer awareness.

---

##  Hardware Components
- Raspberry Pi 4 (4GB RAM)  
- Pi Camera (720×720 resolution, ~1.7 FPS)  
- IR Motion Sensor  
- GSM Module  
- GPIO-controlled deterrent devices (speaker, spray, alarms)  
- LCD Display for local monitoring  

---

##  Deep Learning Models
### Dataset
- Source: Kaggle + Roboflow annotations  
- Classes: Monkey, Elephant, Wild Boar  
- Split: 70% Training, 20% Validation, 10% Test  
- Preprocessing: resized to 640×640, normalized pixel values  
- Augmentation: flipping, rotation, brightness adjustment  

### Model Comparison
| Metric      | YOLOv8 | YOLOv11 |
|-------------|--------|---------|
| mAP@50      | 87%    | 81.9%   |
| Precision   | 90%    | 84.2%   |
| Recall      | 76%    | 74.1%   |
| F1-score    | 82%    | 78.8%   |

- **YOLOv8** → Higher accuracy overall, better precision and recall.  
- **YOLOv11** → Slightly lower metrics but stable performance, optimized for Raspberry Pi deployment.  

---

##  Results
- Wild boar detection → 93% confidence  
- Monkey detection → 92% confidence  
- Elephant detection → 93% confidence  

The system successfully triggered deterrent devices in real-time tests, proving effective for crop protection.

---

## Advantages
- Real-time detection and automated response  
- Energy-efficient (sensor-triggered camera)  
- Selective deterrent activation saves resources  
- Farmer notification via GSM ensures awareness  
- Cost-effective and scalable for agricultural use  

---

##  Future Improvements
- Multi-frame verification for higher reliability  
- Model optimization for faster inference on Raspberry Pi  
- IoT-based networking for large-scale deployment  
- Cloud dashboard for farmer monitoring and analytics  

---

##  Authors
- Krithika S  
- Keerthi Sheevani G  
- Lekhavarshini V  
- Balaji M  

---

##  Reference
Published in: *Proceedings of the 7th International Conference on Intelligent Communication Technologies and Virtual Mobile Networks (ICICV-2026)*  
Paper: **Automated Animal Intrusion Detection and Repellent Activation in Crop Fields**  
ISBN: 979-8-3195-2946-6  

---

##  License
This project is licensed under the **MIT License** — see the LICENSE file for details.
