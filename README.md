# CA_Lab
🧠 CIFAR-10 Image Classification using CNN (TensorFlow)
📌 Project Overview

This project implements a Convolutional Neural Network (CNN) using TensorFlow and Keras to classify images from the CIFAR-10 dataset.

The model is trained to classify 32×32 color images into 10 different categories.

📊 Dataset

We use the CIFAR-10 dataset, which contains:

60,000 color images (32×32 pixels)

10 classes:

Airplane

Automobile

Bird

Cat

Deer

Dog

Frog

Horse

Ship

Truck

50,000 training images

10,000 testing images

Dataset is automatically loaded using:

datasets.cifar10.load_data()
🏗 Model Architecture

The CNN model is built using Sequential() API.

🔹 Architecture Layers

Conv2D (32 filters, 3×3, ReLU)

MaxPooling2D (2×2)

Conv2D (64 filters, 3×3, ReLU)

MaxPooling2D (2×2)

Conv2D (64 filters, 3×3, ReLU)

Flatten

Dense (64 neurons, ReLU)

Dense (10 neurons – Output layer)

⚙️ Model Compilation
model.compile(
    optimizer='adam',
    loss=tf.keras.losses.SparseCategoricalCrossentropy(from_logits=True),
    metrics=['accuracy']
)
🔹 Optimizer

Adam (Adaptive learning optimizer)

🔹 Loss Function

Sparse Categorical Crossentropy
