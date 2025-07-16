🍅 Tomato Leaf Disease Detection — Project Structure & Description
This project is a web-based tool to detect diseases in tomato leaves using a trained CNN model, integrated with a Flask web application.

1. Root Directory: Tomato-Leaf-Project/
The top-level folder that holds everything related to your project.

Contains:
app.py: Flask app (main logic)

requirements.txt: Python packages required to run the app

README.md: Documentation for users or developers

Training/: Folder for model files

static/: Folder for static files like images and CSS

templates/: Folder for HTML templates used in rendering web pages

2. app.py — Flask Backend
Role:
Loads the trained .h5 CNN model

Receives an image upload from the user

Processes and predicts the class of the tomato leaf

Returns the prediction result in an HTML page

Key Functionalities:
@app.route('/'): Renders upload form (index.html)

@app.route('/predict', methods=['POST']): Handles image upload, prediction, and rendering result (result.html)

Model is loaded once at the top using Keras load_model()

3. Training/ — Model Directory
Contains:
tomato_leaf_disease_model.h5: A trained deep learning model for classifying tomato leaf diseases.

Notes:
Should be pre-trained using TensorFlow/Keras.

Not re-trained during runtime; just loaded for inference.

4. templates/ — HTML Pages
This folder contains the web pages shown to the user.

index.html:
A basic form for uploading images

Has a submit button for the user to start prediction

result.html:
Shows:

The predicted class label

The uploaded leaf image

Receives data from Flask and renders with {{ variable_name }} syntax (Jinja2)

5. static/ — Static Resources
Contains all static files Flask can serve directly (CSS, images, etc.).

uploads/:
Stores uploaded images temporarily

Allows them to be shown again on the result page

style.css:
Optional styling for the index.html and result.html pages

6. requirements.txt
Purpose:
Lists the Python packages required
