# 3D Object Detection and Localization Using YOLO and MiDaS for Real-Time Applications

## Project Overview
This project implements a vision-based 3D object detection and localization system using a single monocular camera. By integrating YOLOv8 for object detection and MiDaS for depth estimation, this system achieves real-time performance and accuracy, providing a cost-effective alternative to LiDAR-based solutions.

---

## Features
- **3D Object Detection**: Utilizes YOLOv8 for efficient object detection.
- **Depth Estimation**: Employs MiDaS with a DPT-Hybrid backbone for robust monocular depth estimation.
- **3D Localization**: Calculates real-world object positions using camera intrinsic parameters.
- **Real-Time Performance**: Optimized for computational efficiency with advanced models.

---

## Project Structure

├── Dataset/ 
│ └── image/ # Folder for test images 
├── depth.pth # Pre-trained MiDaS model weights (download required) 
├── yolo.pt # Pre-trained YOLOv8 model weights (download required) 
├── 3D_Detection.ipynb # Notebook for 3D object detection and localization 
├── YOLO_train.ipynb # Notebook for YOLOv8 training 
├── Depth_train.ipynb # Notebook for depth estimation model training 
├── README.md # Project documentation 
└── Project Report.pdf # Detailed project report


---

## Setup Instructions
1. **Test Image Preparation**: Place your test images in the `Dataset/image` folder. (Currently, it includes one sample image.)
2. **Download Pre-Trained Models**: 
   - [depth.pth](https://drive.google.com/file/d/1Y72j-CAfJIQt4WkC4brp_TB7W7x7Dt3G/view)
   - [yolo.pt](https://drive.google.com/file/d/1Y72j-CAfJIQt4WkC4brp_TB7W7x7Dt3G/view)
   - Save these files in the project’s root directory.
3. **Run the Notebook**: Execute `3D_Detection.ipynb` to generate a video with 3D coordinates for objects detected in the test images.
4. **Adjust File Paths**: Ensure all file paths in the code match your directory structure.

---

## Results
- The output video contains detected objects with their 3D positions displayed in real-time.
- Example Metrics:
  - YOLOv8 Medium (No Data Augmentation): **Precision: 0.9418**, **Recall: 0.8908**, **mAP50: 0.9391**.
  - MiDaS depth estimation achieves robust predictions with Vision Transformer backbones.

---

## Requirements
- Python 3.8+
- Dependencies:
  - `torch`, `torchvision`
  - `opencv-python`
  - `matplotlib`
  - `numpy`
- Ensure GPU support for faster computations.

---

## Authors
- **Aditya Aspat** - [aspat.a@northeastern.edu](mailto:aspat.a@northeastern.edu)
- **Jay Jajoo** - [jajoo.j@northeastern.edu](mailto:jajoo.j@northeastern.edu)
- **Asmita Chetlapalli** - [chetlapalli.a@northeastern.edu](mailto:chetlapalli.a@northeastern.edu)

---

## Acknowledgments
This project was developed at Northeastern University as part of an academic initiative to explore cost-effective 3D detection using YOLO and MiDaS models.

---

## Citation
If you use this codebase, please cite the associated project report:
