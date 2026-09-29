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

## 📸 Screenshots

### Scanner Interface



![NutriScore Scanner](nutriscore-scanner.png)
