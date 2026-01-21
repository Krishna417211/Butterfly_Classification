# Butterfly_Classification

Butterfly Image Classification
1. The Core Objective
The goal of this project is to automate the identification of 75 different butterfly species from digital images. In the biological world, many species look nearly identical (such as the Monarch and the Viceroy); this project uses Deep Learning to detect tiny textures, wing patterns, and color gradients that a human might miss.

2. Dataset
The project uses the Butterfly Image Classification dataset from Kaggle.

Total Images: 6,499 files.

Total Classes: 75 species.

Pre-processing: Images are resized to 224x224x3 and normalized to a range of [0,1].

3. Model Architecture
The model is a custom Convolutional Neural Network (CNN) built using the Keras Sequential API.

Layer Type	Filters/Units	Details
Conv2D	32	3x3 Kernel, ReLU activation
MaxPooling2D	-	2x2 Pool size, Stride 2
Conv2D	64	3x3 Kernel, ReLU activation
MaxPooling2D	-	2x2 Pool size, Stride 2
Conv2D	128	3x3 Kernel, ReLU activation
MaxPooling2D	-	2x2 Pool size, Stride 2
Flatten	-	-
Dense	256	ReLU activation
Dense	128	ReLU activation
Dense (Output)	75	Softmax activation

Export to Sheets

Total Parameters: 22,287,243 (Trainable).

4. Training and Performance
Optimizer: Adam

Loss Function: Sparse Categorical Crossentropy

Batch Size: 32

Epochs: 10

Results
The model achieved a final validation accuracy of 87.14%.

5. Project Structure
The notebook includes a full pipeline:

Kaggle Integration: Scripts to download and unzip the dataset directly into Google Colab.

Data Organization: Automated script to sort a flat directory of images into class-named folders based on a CSV mapping.

Data Augmentation/Splitting: Uses an 80/20 train/validation split with shuffling.

Training & Evaluation: Comprehensive model summary and accuracy reporting.

6. How to Use
Clone this repository.

Upload your kaggle.json to access the dataset.

Run the notebook to prepare the directory structure and train the model.

Use the trained model to predict species from new images.

Author: Krishna Priya Biju
