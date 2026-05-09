# MNIST Handwritten Digit Clustering with MiniBatchKMeans

## Description
This program uses K-Means clustering (MiniBatchKMeans for efficiency) to analyze the MNIST dataset of handwritten digits. The goal is to cluster similar digits together without prior knowledge of their labels, and then evaluate the clustering performance by mapping cluster IDs to actual digit values.

## Key Features
- **Data Loading:** Imports the MNIST dataset using Keras.
- **Data Preprocessing:** Normalizes pixel values and reshapes 28x28 images into 1-dimensional arrays for clustering algorithms.
- **Clustering:** Utilizes MiniBatchKMeans to cluster the preprocessed image data.
- **Cluster Identification:** Develops a method to map each cluster to the actual digit it represents by looking up the true labels (y_train).
- **Accuracy Evaluation:** Calculates and displays the accuracy score of the clustering, comparing the mapped cluster labels with the true digit labels.
- **Hyperparameter Tuning:** Explores the impact of varying the number of clusters on the overall accuracy.
- **Visualization:** Visualizes the centroids of the clusters as reconstructed 28x28 images, providing insight into what each cluster represents.

## Setup and Installation
To run this notebook, install the following Python libraries:

```bash
pip install numpy scikit-learn matplotlib keras tensorflow
```

## How to Run
1.  Clone the repository or download the notebook file.
2.  Open the notebook in a Jupyter environment.
3.  Run all cells sequentially.

## Code Overview
- Imports necessary libraries (`matplotlib`, `numpy`, `sklearn.cluster.MiniBatchKMeans`).
- Loads the MNIST dataset (`x_train`, `y_train`, `x_test`, `y_test`).
- Preprocessess the image data - Normalizes and reshapes the `x_train` data.
- Initializes and fits `MiniBatchKMeans` with a default of 10 clusters.
- Contains the logic to map cluster labels to digit values and creates `digit_values` array.
- Compares predicted vs. actual digit values for a small sample.
- Calculates and prints the accuracy score for 10 clusters.
- Iterates through various `n_clusters` values to show how accuracy changes.
- Extracts, reshapes, and visualizes the cluster centroids as images.

## Results
This program initially achieved 55.5% accuracy with 10 clusters. When we increased the clusters to 400, the accuracy went up to 91.2%. Here is a visualization of a few samples.
<img width="454" height="355" alt="image" src="https://github.com/user-attachments/assets/5255a5d8-1d75-4cc6-b538-ae0b738fbef8" />

