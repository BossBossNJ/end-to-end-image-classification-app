# End-to-End Image Classification App

This application provides an end-to-end solution for image classification using deep learning techniques. The app allows users to upload images and receive predictions based on a trained model.

## Installation

Use the package manager pip to install the required packages.

```bash
pip install -r requirements.txt
```

## Project Structure

```python
image_classification_app/
├── app.py/                      
│   ├── model/
│   ├── templates/             
│   └── main.py   
├── requirements.txt       
├── Dockerfile   
├── docker-compose.yml
└── notebook-code/                      
    ├── image/
    ├── model/             
    ├── main-test-api.py   
    ├── test_inferance_from_api.ipynb
    └── train_image_classification_model.ipynb
```


## Pipeline
### 0. Prepare Dataset
Download the image classification data from the following Kaggle links:

[Animal Image Dataset - 90 Different Animals](https://www.kaggle.com/datasets/iamsouravbanerjee/animal-image-dataset-90-different-animals/data)

[Mammals Image Classification Dataset - 45 Animals](https://www.kaggle.com/datasets/asaniczka/mammals-image-classification-dataset-45-animals)
### 1. Build and Train Model
You can build and train the image classification model by following the Google Colab notebook:

[Training Colab Notebook](https://colab.research.google.com/drive/1GQw_fGLMA0eOWN4uClyvBVkQgmVhXiwY?usp=sharing)

Alternatively, you can use the ```train_image_classification_model.ipynb``` notebook provided in the repository.

### 2. Build FastAPI for Inference

please load model : [weight model](https://drive.google.com/file/d/1u43IUvR1nd1gmYUQH-88WJuB8n2uzrjZ/view?usp=sharing) and move into model directory

To run the FastAPI application for animal image classification inference, load the model and execute the following command:

```bash
cd notebook-code
fastapi dev main-test-api.py
```
You can test the API for model inference using the ```test_inference_from_api.ipynb``` notebook.

### 3. Create Web App for Inference and Build Docker
To run the web application with Docker, use the following command:
```bash
docker compose up
```
