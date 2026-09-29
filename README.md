# 🥗 NutriScore Barcode Scanner

A web-based nutrition scanning application that uses a device camera to detect food-product barcodes and retrieve nutritional information and Nutri-Score data.

The project provides a simple interface where users can scan a packaged food product and retrieve available product and nutrition information.

---

## 📌 Project Overview

NutriScore Barcode Scanner connects camera-based barcode detection with food-product data APIs.

The application captures frames from the user's camera, sends them to a Python Flask backend, attempts to detect the barcode, and then uses the detected product barcode to retrieve product information.

### Basic workflow

Camera
↓
Barcode Detection
↓
Barcode Number
↓
Food Product API
↓
Product Information
↓
Nutrition / Nutri-Score
↓
Result displayed to the user

---

## ✨ Features

- 📷 Camera-based barcode scanning
- 🔎 Barcode detection using Python
- 🥗 Food product lookup
- 📊 Nutritional information retrieval
- 🏷️ Nutri-Score information
- 🔄 Product information retrieved through an external API
- 🌐 Flask-based web application
- 💻 Separate local and production project configurations

---
## 🏗️ Architecture / How It Works

The application follows a simple client-server architecture:

1. **Camera Input** – The browser accesses the device camera.
2. **Frame Capture** – Camera frames are captured continuously.
3. **Barcode Detection** – Captured frames are sent to the Flask backend for barcode detection.
4. **Barcode Extraction** – When a barcode is detected, its numeric value is extracted.
5. **Product Lookup** – The barcode is used to retrieve product information from the food-product API.
6. **Nutrition Data** – Available nutritional information and Nutri-Score data are extracted from the API response.
7. **Result Display** – The product and nutrition information is returned to the web interface.

### Architecture Flow

```text
Browser Camera
      ↓
Camera Frames
      ↓
Flask Backend
      ↓
Barcode Detection
      ↓
Barcode Number
      ↓
Food Product API
      ↓
Product / Nutrition Data
      ↓
Web Interface
---

## 🛠️ Tech Stack

### Frontend
- HTML
- CSS
- JavaScript
- Browser Camera API

### Backend
- Python
- Flask
- OpenCV

### API
- Open Food Facts API

### Development
- Git
- GitHub
- Local Flask development server
---

## 🔎 Barcode Detection

The application uses the device camera to capture frames and sends the captured image data to the Flask backend.

The backend processes the image and attempts to detect a food-product barcode. When a barcode is successfully detected, the barcode number is extracted and used for product lookup.

### Detection Flow

```text
Camera
  ↓
Captured Frame
  ↓
Barcode Detection
  ↓
Barcode Number
  ↓
Product Lookup
---

## 🌐 Open Food Facts API

The application uses the Open Food Facts API to retrieve food-product information using the detected barcode.

After a barcode is detected, the barcode number is sent to the API. The application can then retrieve available product information such as:

- Product name
- Ingredients
- Nutritional values
- Nutri-Score information
- Other available product details

The availability of information depends on whether the scanned product is present in the Open Food Facts database.
---

## 🏷️ Nutri-Score

The application retrieves Nutri-Score information from the Open Food Facts API when it is available for the scanned product.

The Nutri-Score provides a quick indication of the nutritional quality of a food product and can help users understand the product's nutritional information more easily.

---

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone https://github.com/pitamber-code/Nutriscore-Barcode_Scanner.git
cd Nutriscore-Barcode_Scanner
### 2. Install dependencies

Install the required Python packages:

```bash
pip install flask opencv-python numpy pyzbar requests
```






### 3. Run the application

Start the Flask development server:

```bash
python app.py
---

## 🔍 Example

### Input

A packaged food product with a barcode.

### Processing

```text
Barcode
   ↓
Open Food Facts API
   ↓
Product Information
   ↓
Nutrition / Nutri-Score Data
   ↓
Displayed to User
---

## ⚠️ Known Limitations

- Barcode detection depends on camera quality, lighting, barcode size, and positioning.
- Small or curved barcodes may be difficult to detect.
- Products not available in Open Food Facts may not return complete information.
- Product information depends on external API data.
- Camera permission is required.
- Internet connectivity is required for product lookup.
- The project currently uses Flask's development server for local execution.
---

## 👨‍💻 My Contribution

I worked on the development of the NutriScore Barcode Scanner, including the Flask application structure, camera-based barcode scanning workflow, barcode detection integration, product information retrieval, and presentation of nutrition information.

I also worked on running and testing the application locally and troubleshooting the flow between the browser camera, Flask backend, barcode detection, and product API.
---

## 🚀 Future Improvements

- Improve barcode detection accuracy under different lighting and camera conditions.
- Add manual barcode entry as a fallback.
- Support additional barcode formats.
- Improve handling of products with incomplete information.
- Add automated tests for barcode detection and API responses.
- Add product comparison features.
- Improve the mobile camera experience.
- Deploy a public production version.
## 📸 Screenshots

### Scanner Interface



![NutriScore Scanner](nutriscore-scanner.png)
