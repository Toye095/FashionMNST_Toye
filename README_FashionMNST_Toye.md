# Project: Fashion MNIST Image Classifier

## Table of Contents
* Overview
* Features
* Installation
* Folder Structure
* Implementation Steps
* How to Run
* Usage
* Requirements
* Credits

## 1. Overview
This project implements a Fashion MNIST classifier using a pre-trained convolutional neural network (CNN) and was packaged into an app is deployed using Gradio. The Fashion MNIST Classifier predicts the type of clothing item in an image, trained on the Fashion MNIST dataset. The categories are T-shirt/top, Trouser, Pullover, Dress, Coat, Sandal, Shirt, Sneaker, Bag and Ankle boot.

## 2. Features
* Accepts user-uploaded images.
* Automatically resizes and preprocesses images for prediction.
* Outputs the predicted category with a confidence score.
* Lightweight and easy to run locally both on lab and terminals environments.
    
## 3. Installation
   * 1. Prerequisite: Python 3.8 or higher
   * 2. Step1: clone git repository and change directory as applicable 

## 4. Folder Structure
 
    Fashion_MNIST_Toye/                       # Main Folder
    │
    ├── app.py / app.ipynb                    # Main application script and notebook
    |__ dataset.py / dataset.ipynb            # dataset loading and preprocessing script and notebook
    |__ model.py / model.ipynb                # CNN model build  script and notebook
    |__ train.py / train.ipynb                # model training script and notebook
    |__ predict.py / predict.ipynb            # label prediction script and notebook
    |__ save_test_image.ipynb                 # downnload test fashion images notebook
    ├── requirements.txt                      # Python dependencies
    ├── README_FashionMNST_Toye.md            # Project documentation
    ├── saved_model/                          # Folder containing the trained model
    │   └── fashion_mnist_cnn.keras           # saved keras model
    ├── saved_test_images/                    # Folder containing saved test fashion images (to test the app)
  
## 5. Implementation Steps
   * a. Train the CNN Model: A CNN was trained on the Fashion MNIST dataset to classify clothing items into one of ten categories. The trained model is saved as fashion_mnist_cnn.keras in the saved_model directory. (Pre-trained model provided.)
   * b. Build the Gradio Interface: The Gradio library was used to build a GUI for the app. The user uploads an image, which is resized and preprocessed before being fed into the model.
   * c. Preprocessing: Images are resized to 28x28 pixels and converted to grayscale and normalized to the range [0, 1].
   * d. Prediction: The preprocessed images are passed to the model which predicts the class with the highest probability and outputs the result.
   * e. Deployment: Ran the app locally using Gradio.
   
## 6. How to Run

### Method 1: Running .py Scripts on Terminal

   * i. Install Dependencies `pip install -r requirements.txt`
   * ii. Start the app `python app.py`
   * iii. Open Gradio interface using the url generated `http://127.0.0.1:7860`
   * iv. Click on image and acess the saved_test_images which should have been downloaded in your directory 
   * v. Select an image, upload and submit to classify: See example of interface below
   
   ![image.png](attachment:image.png)
   
### Method 1: Running .ipynb on notebook 

   * i. Run the ipynb files in this order: dataset.ipynb -> model.ipynb -> train.ipynb -> predict.ipynb -> app.ipynb
   * ii. Open Gradio interface using the url generated `http://127.0.0.1:7860`
   * iii. Click on image and acess the saved_test_images which should have been downloaded in your directory 
   * iv. Select an image, upload and submit to classify: See example of interface below   
    ![image.png](attachment:image.png)
    
## 7. Usage
* Steps to Use:
   * 1. Upload an image of a clothing item.
   * 2. Click Submit.
   * 3. View the predicted category and confidence score.
* Example:
* - Input: An image of a shoe.
* - Output: Predicted: Sneaker (Confidence: 0.95)

## 8. Requirements
* Python Dependencies (requirements.txt):
    * gradio==3.23.0
    * tensorflow==2.13.0
    * numpy==1.23.5
    * Pillow==9.2.0
    
## 9. Credits
* Fashion MNIST Dataset: Zalando Research.
* Gradio: Gradio Documentation.    


```python

```
