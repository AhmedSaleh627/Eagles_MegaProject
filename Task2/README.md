# YOLO Shape, Letter and Color Detection

This project utilizes YOLO (You Only Look Once) for shape detection, color identification, and Optical Character Recognition (OCR) to identify letters within shapes. It evaluates its performance on 20 sample images.

## Overview

The code accomplishes the following tasks:

- **Object Detection with YOLO**:
  - Uses YOLO to detect shapes and draws bounding boxes.
  - Displays processed images with bounding boxes.

- **Shape and Color Extraction**:
  - Extracts cropped regions of detected shapes.
  - Determines the dominant color of each shape.
  - Predicts colors using a pre-trained model.

- **Optical Character Recognition (OCR)**:
  - Applies OCR to recognize letters within shapes.
  - Enhances recognition by rotating images.
  - Records the most recognized letter.

- **Letter and Color Prediction**:
  - Predicts shape and letter colors using a pre-trained model.
  - Displays predicted colors as color-coded boxes.
  - Provides letter predictions and their predicted colors.

## Prerequisites

Before running the code, ensure you have the following dependencies installed:

- Ultralytics: YOLO-based object detection.
- EasyOCR: Optical Character Recognition.
- OpenCV: Computer Vision library.
- Pandas and NumPy: Data manipulation.
- Joblib: Library for model loading.
- Google Colab (optional): For running in a Colab environment.

## Evaluation

The code evaluates the detection performance on 20 samples with the following results:

- YOLO detection accuracy: 100%
- Shape color detection accuracy: 95%
- Letter detection accuracy: 70%
- Letter color detection accuracy: 70%

## License

This project is licensed under the MIT License.

## Acknowledgments

- The YOLO model is based on Ultralytics YOLOv8.
- Optical Character Recognition is performed using EasyOCR.
- Color classification is done using a random forest model.
- Special thanks to Google Colab for providing a convenient environment for running this code.
