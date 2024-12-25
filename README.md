# -NLP-ML-
Natural Language Processing and Harware
Machine Learning Hardware Project
Potato Leaf Disease Identification and Classification

This project provides a Streamlit-based web application to identify and classify diseases in potato leaves. Users can upload an image of a potato leaf, and the app predicts the type of disease present along with a confidence score and recommended actions. The classification model was trained on Google Colab and deployed for use in this application.

Features
- Disease Prediction: The app can classify potato leaves into the following categories:
  - Potato Early Blight
  - Potato Late Blight
  - Healthy
- Confidence Score: The prediction is accompanied by a confidence percentage.
- Recommendations: Offers actionable steps based on the disease identified.
- User-Friendly Interface: A simple and clean interface for uploading images and viewing results.

Application Workflow
1. Upload Image: Users upload an image of a potato leaf in `.jpg` format.
2. Display Image: The uploaded image is displayed for confirmation.
3. Predict Disease:
   - The app preprocesses the image.
   - The pre-trained model predicts the disease class.
   - The app displays the prediction, confidence score, and recommended actions.

Technical Details
- Model Training:
  - The model was trained on Google Colab using TensorFlow/Keras.
  - The dataset used includes labeled images of potato leaves with Early Blight, Late Blight, and Healthy categories.
- Deployment: The model was exported as an H5 file (`potatoes.h5`) and integrated into a Streamlit application.
- Preprocessing: Images are resized to 256x256 pixels and normalized before being fed into the model.

Prerequisites
1. Python 3.7+
2. Required Python Libraries:
   - `streamlit`
   - `tensorflow`
   - `numpy`
   - `Pillow`
   - `matplotlib`

Key Functions
`predict_class(image)`
- Loads the pre-trained model.
- Preprocesses the uploaded image.
- Predicts the class of the image.
- Returns:
  - Predicted class (e.g., "Potato Early Blight").
  - Confidence score (e.g., 95.5%).
  - Recommended action (e.g., "Use fungicides for early blight.").

`main()`
- Handles the application logic including image upload, display, and calling the `predict_class` function to show results.

