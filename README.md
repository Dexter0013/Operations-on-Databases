<p align="center"> <h1 align="center">🚀 EfficientNetB7 Image Classification & Logging Pipeline</h1> <p align="center">Classify images using TensorFlow · Log results in CSV · Analyze with Pandas · Store in MySQL</p> </p>

<p align="center"> <img src="https://img.shields.io/badge/tensorflow-2.14%2B-orange?style=flat-square" /> <img src="https://img.shields.io/badge/EfficientNetB7-ImageNet-brightgreen?style=flat-square" /> <img src="https://img.shields.io/badge/Pandas-Data%20Analysis-blue?style=flat-square" /> <img src="https://img.shields.io/badge/MySQL-Storage-lightgrey?style=flat-square" /> <img src="https://img.shields.io/badge/CSV-Logging-yellow?style=flat-square" /> <img src="https://img.shields.io/badge/Streamlit-ready-red?style=flat-square" /> </p>

📦 Features
🔍 Image classification with EfficientNetB7 (pretrained on ImageNet)

📝 Logs predictions with timestamp and image path to CSV

📊 Performs data analysis using Pandas

🗄️ Optionally stores results in a MySQL database

🧱 Scalable foundation for batch processing or dashboard integration

📁 Project Structure
<details> <summary><strong>📂 root/</strong></summary>

Main project folder containing all files and subdirectories.

</details>

<details> <summary><strong>📁 data/</strong></summary>

human1.jpg – Input image used for prediction

prediction_results_imgPath.csv – Log file storing predictions along with timestamp and image metadata

</details>

<details> <summary><strong>📁 scripts/</strong></summary>

image_predictor.py – Core script performing image preprocessing, EfficientNetB7 prediction, CSV logging, and optional MySQL storage

</details>

📋 Workflow Steps
<details> <summary><strong>🔍 1. Image Inference</strong></summary>

Load an input image (e.g., JPEG format).

Resize it to 600×600 pixels, as required by EfficientNetB7.

Use TensorFlow's pretrained EfficientNetB7 to predict top classes.

Decode predictions to get ImageNet ID, label, and confidence score.

</details>

<details> <summary><strong>📝 2. Log Prediction</strong></summary>

Append the prediction to a CSV file with:

ImageNet ID

Label

Score

Date & Time

Image path

Creates the file and header if not present, ensuring structured logging.

</details>

<details> <summary><strong>📊 3. Analyze with Pandas</strong></summary>

Load CSV data into a Pandas DataFrame.

Analyze prediction history:

🔢 Count label frequency

🏆 Sort by confidence scores

📅 View prediction trends over time

Optionally plot results using Matplotlib for quick insights.

</details>

<details> <summary><strong>🗄️ 4. Store in MySQL</strong></summary>

Create a MySQL database and table schema matching the DataFrame columns.

Insert rows from the DataFrame into the MySQL table using Python connectors.

Enables long-term storage, querying, and dashboard integration.

</details>

🔧 Tech Stack
<details> <summary><strong>🧠 TensorFlow / Keras</strong></summary>

Used for implementing the EfficientNetB7 model pretrained on ImageNet. Handles image preprocessing, prediction, and model loading.

</details>

<details> <summary><strong>📊 Pandas</strong></summary>

Performs structured data manipulation. Used to load, filter, sort, and analyze prediction logs saved in CSV format.

</details>

<details> <summary><strong>🗂️ CSV</strong></summary>

Serves as a lightweight, append-only format for logging predictions with labels, scores, timestamps, and image paths.

</details>

<details> <summary><strong>🗄️ MySQL</strong></summary>

Stores prediction records in a relational schema for scalable access. Enables integration with dashboards and advanced querying.

</details>

<details> <summary><strong>📈 Matplotlib (optional)</strong></summary>

Used to visualize trends in prediction data—such as most frequent labels or prediction counts over time.

</details>

<details> <summary><strong>☁️ Google Colab + Drive (optional)</strong></summary>

Provides a cloud-based environment to execute the workflow and store files persistently in Google Drive.

</details>
