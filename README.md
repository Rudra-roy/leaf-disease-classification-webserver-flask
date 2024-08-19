---

# **YOLOv8 Image Classifier Web App**

## **Overview**

This project is a web-based application that allows users to upload an image and classify it using a custom-trained YOLOv8 classifier model. The app provides a simple and user-friendly interface for image classification tasks, leveraging the power of transfer learning and deep learning for accurate predictions.

### **Features**

- **Image Uploading**: Users can upload an image through a simple interface.
- **Real-time Classification**: Once an image is uploaded, it is processed and classified using a custom-trained YOLOv8 model.
- **Dynamic Results**: The app provides a prediction with a smooth sliding animation and displays the uploaded image along with the classification result.
- **Responsive Design**: The web app is fully responsive and can be accessed on various devices, including desktops, tablets, and mobile phones.

### **Technology Stack**

- **Backend**: Flask - A lightweight WSGI web application framework for Python.
- **Frontend**: HTML, CSS, JavaScript - For building a responsive and interactive user interface.
- **Deep Learning**: YOLOv8 - A state-of-the-art object detection and classification model.
- **Deployment**: Can be deployed on cloud platforms like Heroku or AWS.

## **Project Structure**

```
web-app/
│
├── static/
│   ├── styles.css         # Styling for the web app
│
├── templates/
│   ├── index.html         # Home page template
│   └── result.html        # Result page template
│
├── uploads/
│   └── (Uploaded images are stored here)
│
├── yolov8_model/
│   └── your_model_weights.pt  # Trained YOLOv8 model weights
│
├── app.py                # Main Flask application

```

### **1. `app.py`**

The core of the web application, built using Flask. It handles the routing, file uploads, and integration with the YOLOv8 model for image classification.

### **2. `templates/`**

This directory contains the HTML templates for the web pages:
- **`index.html`**: The home page where users can upload an image.
- **`result.html`**: The result page where the prediction and uploaded image are displayed.

### **3. `static/`**

Contains the `styles.css` file, which is responsible for the styling of the web app. It includes custom styles for buttons, animations, and overall layout.

### **4. `uploads/`**

Stores the images uploaded by users temporarily for processing and display.

### **5. `yolov8_model/`**

This directory contains the YOLOv8 model weights (`your_model_weights.pt`). The model is loaded from here to make predictions.

## **How It Works**

1. **Pre-trained Model Loading**: The app loads a pre-trained YOLOv8 model, fine-tuned for a specific classification task (e.g., plant disease detection).

2. **Image Upload**: Users upload an image through the web interface. The image is saved in the `uploads/` directory.

3. **Model Prediction**: The uploaded image is passed through the YOLOv8 model, which outputs a prediction label based on the learned features.

4. **Display Results**: The result page displays the prediction along with the uploaded image. A smooth sliding animation enhances the user experience.

5. **Try Again**: Users can easily navigate back to the home page to upload another image.

## **Installation and Setup**

### **Prerequisites**

- Python 3.7 or higher
- `pip` for managing Python packages

### **Installation Steps**

1. **Clone the Repository**

   ```bash
   git clone https://github.com/yourusername/yolov8-image-classifier.git
   cd yolov8-image-classifier
   ```

2. **Create a Virtual Environment**

   ```bash
   python3 -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install Dependencies**

   ```bash
   pip install -r requirements.txt
   ```

4. **Download Your Trained YOLOv8 Model**

   Place your custom-trained YOLOv8 model weights (`your_model_weights.pt`) in the `yolov8_model/` directory.

5. **Run the Application**

   ```bash
   python app.py
   ```

6. **Access the Web App**

   Open your browser and go to `http://127.0.0.1:5000/` to access the web app.

## **Customization**

You can easily customize this web app to fit your specific needs:

- **Change the Model**: Replace the YOLOv8 model weights in the `yolov8_model/` directory with your own trained model.
- **Modify the Interface**: Update the HTML and CSS in the `templates/` and `static/` directories to change the look and feel of the web app.
- **Deploy the App**: Follow deployment guidelines to host the app on platforms like Heroku, AWS, or others.

## **Contributing**

Contributions are welcome! If you have any ideas, suggestions, or bug reports, please open an issue or submit a pull request.

## **License**

This project is licensed under the MIT License. See the `LICENSE` file for more details.
