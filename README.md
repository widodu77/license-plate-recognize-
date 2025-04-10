License Plate Recognize
-----------------------
An Automatic License Plate Recognition (ALPR) system implemented in Python. This project uses computer vision and deep learning techniques to detect license plates in vehicle images and extract alphanumeric characters using Optical Character Recognition (OCR).

Table of Contents
-----------------
1. Overview
2. Features
3. Installation
4. Usage
5. Project Structure
6. Details
7. Requirements
8. Contributing
9. License
10. Acknowledgements

Overview
--------
The License Plate Recognize project provides an end-to-end solution for detecting and reading vehicle license plates. The system is designed to:
- Detect license plates from images using OpenCV.
- Preprocess and extract regions of interest (ROIs) that contain license plates.
- Leverage a fine-tuned deep learning model (based on TensorFlow’s Keras API and InceptionResNetV2) for enhanced detection performance.
- Use PyTesseract to perform OCR and extract the text from the detected license plates.

The project also includes modules for parsing XML annotation files and converting them into CSV format to prepare training data.

Features
--------
- Automatic Plate Detection: Detects license plates from images using OpenCV-based image processing techniques.
- Deep Learning Integration: Uses a customized model built upon a pre-trained InceptionResNetV2 to improve detection accuracy.
- OCR-Based Recognition: Applies PyTesseract to extract and recognize text from the license plate regions.
- Data Preprocessing: Includes functionality to convert XML annotation files to CSV format for easier data handling.
- Visualization: Uses Plotly and Matplotlib to visualize detection results and performance metrics.

Installation
------------
Ensure you have Python 3.6+ installed. Follow these steps to get started:

1. Clone the Repository:
   git clone https://github.com/widodu77/license-plate-recognize-.git
   cd license-plate-recognize-

2. (Optional) Create a Virtual Environment:
   python -m venv venv
   Activate the virtual environment as appropriate for your operating system.

3. Install the Required Dependencies:
   pip install -r requirements.txt

4. Install the Tesseract OCR Engine:
   PyTesseract requires the Tesseract OCR engine. Install it as follows:
   - Windows: Download from https://github.com/UB-Mannheim/tesseract/wiki
   - macOS: Use Homebrew with "brew install tesseract"
   - Linux: Install via your package manager (e.g., sudo apt-get install tesseract-ocr)

Usage
-----
1. Data Preparation:
   - Place your vehicle images in the "data/images/" folder.
   - Store any XML annotation files in the "data/annotations/" folder.
   - Use the provided scripts to convert XML annotations to CSV if required.

2. Running the Recognition Pipeline:
   Execute the main pipeline script to detect license plates, extract the plate regions, perform OCR, and display results:
   python src/main.py

3. Model Training (Optional):
   To fine-tune or train the deep learning model on your own dataset, refer to "src/model.py". This script includes TensorBoard callbacks for monitoring training progress.

Project Structure
-----------------
A typical structure for the project is as follows:

license-plate-recognize-
├── data
│   ├── images         
│   └── annotations    
├── models            
├── src
│   ├── main.py        
│   ├── utils.py       
│   └── model.py       
├── requirements.txt   
└── README.txt         

Details
-------
Key components of the project include:

- Image Processing: Uses OpenCV and scikit-image to load and process images, and to extract regions of interest.
- Deep Learning Model: Utilizes TensorFlow’s Keras API with a pre-trained InceptionResNetV2 backbone, further customized for license plate detection.
- OCR Integration: Applies PyTesseract to perform Optical Character Recognition on the detected license plate regions.
- Annotation Parsing: Employs xml.etree.ElementTree to read XML files and extract bounding box coordinates, converting them into CSV format.
- Visualization: Uses Plotly and Matplotlib to visualize detection results and monitor training metrics.

Requirements
------------
The project requires the following libraries, which are also listed in requirements.txt:
- opencv-python
- numpy
- pandas
- tensorflow
- pytesseract
- plotly
- matplotlib
- scikit-image
- scikit-learn

Contributing
------------
Contributions are welcome. To contribute:
1. Fork the repository.
2. Create a new branch for your modifications.
3. Submit a pull request describing your changes.
4. Ensure that your code adheres to the project's guidelines and passes all tests.

License
-------
This project is open-source and is available under the MIT License.

Acknowledgements
----------------
Special thanks to the developers and maintainers of the following:
- OpenCV (https://opencv.org/)
- TensorFlow (https://www.tensorflow.org/)
- PyTesseract (https://pypi.org/project/pytesseract/)
- Plotly (https://plotly.com/)
- Matplotlib (https://matplotlib.org/)
- Scikit-image (https://scikit-image.org/)
- Scikit-learn (https://scikit-learn.org/)

Enjoy exploring, using, and contributing to the License Plate Recognize project!
