# B-W-to-colour-ML-project
This project is developed to colourize a BnW image .
This Black & White Image Colorization project is implemented in Jupyter Notebook using a pre-trained Deep learnig model developed by  [this guide](https://github.com/richzhang/colorization) , using OpenCV Libraries.
The pre-trained convolutional neural network (CNN) model predicts realistic color information from a grayscale image.

- [Introduction](#introduction)
- [Lab Color Space](#lab-color-space)
- [How It Works](#how-it-works)
- [Setup & Installation](#setup--installation)
- [How to Run (Jupyter Notebook)](#how-to-run-jupyter-notebook)
- [Sample Results](#sample-results)
- [GUI Application (Optional)](#gui-application-optional)
- [References](#references)


## Introduction

Image colorization is the process of adding color to grayscale images.  
This project uses a deep learning model (trained on ImageNet) to automatically colorize black & white images with minimal user input.


## Lab Color Space

Unlike RGB, the **Lab color space** separates lightness (L) from color information (a, b):

- **L channel:** Lightness (grayscale)
- **a channel:** Green–Red color component
- **b channel:** Blue–Yellow color component

The grayscale part of the image is encoded in the L channel, making Lab ideal for colorization tasks.

---

## How It Works

1. **Input:** A black & white (grayscale) image.
2. **Preprocessing:** Convert the image to Lab color space and extract the L channel.
3. **Model Prediction:** Use a pre-trained CNN to predict the a and b color channels.
4. **Postprocessing:** Combine the original L channel with the predicted a and b channels.
5. **Output:** Convert back to RGB and display/save the colorized image.

---

## Setup & Installation

1. **Clone this repository** or download the files.
2. **Install required libraries:**

    ```python
    pip install numpy opencv-python matplotlib pillow
    ```

3. **Download pre-trained model files:**  
   Place these files as shown above.
   - `pts_in_hull.npy`
   - `models/colorization_deploy_v2.prototxt`
   - `models/colorization_release_v2.caffemodel`

   If you need help downloading, see instructions in the notebook or [this guide](https://github.com/richzhang/colorization).

---

## How to Run (Jupyter Notebook)

1. **Open the notebook** (`BlackWhite_Colorization.ipynb`) in Jupyter Notebook or JupyterLab.
2. **Run each cell in order.**  
   - The notebook will guide you through loading the image, running the model, and displaying the result.
3. **Replace `new.jpg`** with your own grayscale image to colorize your own photos.

---

## Sample Results



## GUI Application (Optional)

You can also run a simple GUI to colorize images:

1. **Ensure `gui.py` is present** in your project folder.
2. **Run from terminal:**
    ```
    python gui.py
    ```
3. **Use the GUI to upload and colorize images interactively.**

---

## References

- [Original Model by Richard Zhang et al.](https://richzhang.github.io/colorization/)
- [PyImageSearch: Black and White Image Colorization](https://pyimagesearch.com/2019/02/25/black-and-white-image-colorization-with-opencv-and-deep-learning/)
- [OpenCV DNN Colorization Example](https://github.com/opencv/opencv/blob/master/samples/dnn/colorization.py)

---

**Enjoy bringing color to your memories!**

