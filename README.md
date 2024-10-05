# Tensorflow-Object-Detection-API-and-OpenCV
The project focuses on real-time detection of defective products in a production line using the TensorFlow Object Detection API and OpenCV. It utilizes the SSD-MobileNet-v2 model, fine-tuned on a custom dataset to identify product defects efficiently. The model was trained over multiple steps, with the best results achieved at 10,000 steps, yielding a Mean Average Precision (mAP) of 0.9278 and a recall of 0.9379. This system enhances manufacturing quality control, reducing human intervention, cost, and errors in identifying defective products, and can be applied across industries like FMCG, automotive, and electronics​

Software Components:
1. TensorFlow Object Detection API
2. OpenCV (Open Source Computer Vision Library)
3. SSD-MobileNet-v2 Model
4. Python version 3
5. Jupyter Notebook (Anaconda Navigator)
6. Custom Dataset (Defective Products: four classes)
7. Google Colab
8. Local environment (OS: Windows 10)

Hardware Components:
1. Camera (IPC3614LE-ADF28K)
- 4.0 megapixel CMOS sensor camera for capturing real-time production line images.
- Provides an angle of view of 105.3° (Horizontal), 57° (Vertical).
2. Production Machine (Tortila maker machine)
- CADSON Ruti-making machine used in the evaluation setup for capturing real-time data.
- Specifications: 900 units/hour, PLC HMI & VFD system.
3. Personal Computer
- Running the TensorFlow Object Detection API for processing and analyzing the captured data.
- Specifications: Suitable for model training and image processing.
4. Power Supply (DC 12V)
- Powering the camera used for object detection.
