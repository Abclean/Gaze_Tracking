#  Eye Gaze Direction Detection with Dlib & OpenCV

This project detects the **eye gaze direction** (Left, Center, Right) from images using facial landmarks and visualizes the results using various **graphs and charts**.

# Files Used

- `pic1.jfif`, `pic2.jpg`, `pic3.jpg`: Input face images.
- `shape_predictor_68_face_landmarks.dat`: Pretrained Dlib model for detecting 68 facial landmarks.
- Python script (`.ipynb` or `.py`): Performs image processing, eye detection, gaze analysis, and visualization.

## How to Download the Shape Predictor

You must download the **`shape_predictor_68_face_landmarks.dat`** file to use this project.

Download link:  
https://github.com/davisking/dlib-models/raw/master/shape_predictor_68_face_landmarks.dat.bz2

# Steps:
1. Download and extract the `.bz2` file.
2. Upload `shape_predictor_68_face_landmarks.dat` to your project directory (e.g., in Google Colab, use the file browser).

# How It Works
1. Face Detection: Uses Dlib's HOG-based frontal face detector.
2. Facial Landmark Detection: Loads 68-point landmarks to identify eye regions.
3. Eye Analysis:
   - Extracts left and right eye regions.
   - Applies thresholding to detect pupil position.
   - Estimates gaze direction using the center of mass.
4. Result Display: Adds text labels on images and shows the result.
5. Data Visualization: Uses `matplotlib` to plot:
   - Bar chart of total gaze directions.
   - Pie chart of percentage distribution.
   - Horizontal bar chart.
   - Stacked bar chart (per image).
#Graphs

- Total gaze direction bar chart.
- Pie chart of gaze distribution.
- Horizontal bar chart of gaze frequency.
- Stacked bar chart showing left, center, and right gaze counts per image.

# Dependencies

Install these in your Python environment or Colab:

```bash
pip install opencv-python dlib imutils matplotlib
