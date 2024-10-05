# Tensorflow-Object-Detection-API-and-OpenCV
The project focuses on real-time detection of defective products in a production line using the TensorFlow Object Detection API and OpenCV. It utilizes the SSD-MobileNet-v2 model, fine-tuned on a custom dataset to identify product defects efficiently. The model was trained over multiple steps, with the best results achieved at 10,000 steps, yielding a Mean Average Precision (mAP) of 0.9278 and a recall of 0.9379. This system enhances manufacturing quality control, reducing human intervention, cost, and errors in identifying defective products, and can be applied across industries like FMCG, automotive, and electronics​

**Software Components:**
1. TensorFlow Object Detection API
2. OpenCV (Open Source Computer Vision Library)
3. SSD-MobileNet-v2 Model
4. Python version 3
5. Jupyter Notebook (Anaconda Navigator)
6. Custom Dataset (Defective Products: four classes)
7. Google Colab
8. Local environment (OS: Windows 10)

**Hardware Components:**
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

**Step-by-Step Guide:**
**Step 1: Evaluating and selecting models**
- CNN, R-CNN, Faster R-CNN, and SSD were evaluated based on speed, accuracy, precision, and their ability to perform real-time object detection on the production line. The SSD-MobileNet-v2 model was selected for its balance between detection speed and accuracy, making it suitable for real-time defect detection in a manufacturing environment.
\n**Step 2: Setup the Environment (Dependency Installations and others)**
- Install the necessary libraries and dependencies for the project.
- Python 3.7 or higher
- TensorFlow 2.x, OpenCV, LabelImg, and other libraries such as NumPy, Matplotlib, and Jupyter Notebook.
**Step 3: Collect and Annotate Dataset**
- Collect images of products on the production line, ensuring both defective and non-defective samples.
- Organize these images into specific folders for labeling (e.g., Defective, NotDefective, Burned, NotBurned).
- Annotate images using LabelImg to create bounding boxes around the objects in each image.
- Save the annotations in PASCAL VOC XML format.
**Step 4: Preprocess Data**
- Convert the XML annotations to CSV using a Python script.
- Create TFRecord files to train TensorFlow models, which store both the images and labels in a compressed format.
**Step 5: Select and Download the Pre-Trained Model**
- Download the pre-trained model from TensorFlow Model Zoo (For this project, select SSD-MobileNet-v2 model pre-trained on the COCO dataset).
**Step 6: Configure the Model for Fine-Tuning**
- Modify the pipeline.config file to specify:
- Paths to TFRecord files.
- The number of classes in your dataset.
- The learning rate, batch size, and other hyperparameters.
**Step 7: Train the Model**
**Step 8: Evaluate the Model**
- After training, evaluate the model to check its performance on the test dataset using metrics like Precision, Recall, Intersection over Union (IoU), and Mean Average Precision (mAP).
**Step 9: Export the Trained Model**
- Once satisfied with the model’s performance, export the inference graph so that it can be used in real-time detection.
**Step 10: Implement Object Detection in Real-Time**
- Use OpenCV and the exported model to detect defects in real time from a camera feed.
**Step 11: Test and Deploy**
**Step 12: Maintain and Improve**
- Fine-tune the model further by collecting more data and retraining for better performance.
- Implement additional features such as real-time alerting or integration with factory systems for automated removal of defective products.
