# Image Classification using ResNet50
This project demonstrates how to use the ResNet50 deep learning model for image classification on a variety of input images. The model is pre-trained on the ImageNet dataset, which allows it to classify images into 1,000 categories.

**Project Overview**

Objective
The goal is to classify input images into their respective categories using ResNet50, a powerful convolutional neural network architecture for image recognition tasks.

Workflow
1. **Libraries and Pre-trained Model**
- Libraries:
  - tensorflow.keras for deep learning and model handling.
  - numpy for numerical operations.
  - Pillow (via tensorflow.keras.preprocessing.image) for image processing.
  - IPython.display.Image for displaying images within notebooks.
    
- Pre-trained Model:
  - ResNet50:
    - Pre-trained on ImageNet with 1,000 object categories.
    - Used for predictions without additional training.
2. Steps

  i) Load an Image:
    - Images are resized to 224x224 pixels to match the input size expected by ResNet50. 
  ii) Preprocess the Image:
    - Convert the image to a numpy array using image.img_to_array().
    - Expand dimensions (from (224, 224, 3) to (1, 224, 224, 3)) to match batch input format.
    - Preprocess the pixel values using preprocess_input():
      - Normalizes the image to the format used during ResNet50 training.  
  iii) Predict Categories:
    - Use the model.predict() function to generate predictions.
    - Decode the top 3 predictions with decode_predictions() to map numeric predictions to human-readable class names. 
  iv) Classify Multiple Images:
    - A list of image paths (path_add) is iterated over.
    - Each image is classified, displayed, and the top 3 predictions are printed.
