# Vehicle Detection and Counting with YOLOv11

This hands-on project demonstrates how to train and deploy a **YOLOv11 model** for **vehicle detection and lane-wise traffic density analysis**.  
Students will learn how to apply object detection models in real-world scenarios, specifically to **detect, count, and classify vehicles in video streams** while estimating traffic intensity.

---

## 🎯 Learning Outcomes
By completing this hands-on, students will be able to:
- Train a **YOLOv11** model on a custom vehicle dataset.
- Perform **exploratory data analysis (EDA)** and **data visualization** on object detection datasets.
- Evaluate model performance and generalization.
- Implement a **vehicle counting pipeline** with lane-based logic.
- Estimate **traffic intensity (Smooth vs. Heavy)** in each lane.

---

## 📂 Dataset
The custom dataset used in this project is available on Google Drive:  

👉 [Download Vehicle Dataset](https://drive.google.com/drive/u/1/folders/19YbTcYBnE8OBDADiuqCZtkg785inWoat)  

*(Please ensure you have access before running the notebooks or training the model.)*

---

## 🛠️ Project Workflow
1. **Load Pretrained Model** – Initialize YOLOv11 with pretrained weights.  
2. **Dataset Exploration** – Visualize and analyze annotated vehicle dataset.  
3. **Model Training** – Fine-tune YOLOv11 on custom vehicle data.  
4. **Performance Evaluation** – Compute metrics like mAP and visualize predictions.  
5. **Model Inference** – Run inference on sample images and videos.  
6. **Vehicle Counting Logic** –  
   - Define regions of interest (lanes).  
   - Detect vehicles using YOLOv11.  
   - Count vehicles lane-wise.  
   - Annotate frames with vehicle counts and traffic intensity.  

---

## 🚦 Vehicle Counting Logic
- Each frame is processed using YOLOv11.  
- Lane regions are defined using quadrilaterals.  
- Vehicles are assigned to lanes based on bounding box positions.  
- Lane counts are compared against a **traffic threshold (default: 10 vehicles)**.  
- Traffic intensity is displayed as:  
  - **Smooth** (≤ 10 vehicles)  
  - **Heavy** (> 10 vehicles)  

---

## 📊 Example Output

The pipeline generates a video with:
- Bounding boxes around detected vehicles.
- Lane-wise vehicle counts.
- Traffic intensity labels (Smooth / Heavy) displayed on the frame.

<img width="1789" height="1008" alt="image" src="https://github.com/user-attachments/assets/0e7e3ca2-0cb8-4598-b900-22cd265c8b0c" />

## 📌 Applications

- Smart Traffic Monitoring Systems
- Highway Traffic Management
- Automated Tolling & Surveillance
- Urban Planning & Infrastructure Development
