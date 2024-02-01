
# Image Search System Based on Feature Descriptors

## Project Overview

This project implements an image search system for dermatological images, aiming to find images similar to a given query image. It utilizes feature extraction and similarity measures to compare images based on their visual content. The system processes images, extracts meaningful features, and performs image searches using distance metrics.

## Key Features

- **Data Reading and Example Selection:** Processes a CSV file with image labels, selects 100 examples per class label, and prepares a filtered dataset.
- **Feature Extraction:**
  - **Global HSV Histogram:** Converts images to HSV color space and calculates histograms for each channel to capture color distribution.
  - **Masking:** Applies an elliptical mask to focus on the central part of the images.
  - **Local Binary Pattern (LBP):** Computes LBP for texture analysis and visualizes the texture alongside the grayscale image.
- **Feature Descriptors:**
  - **HSV Description:** Extracts a 3D HSV color histogram as a feature descriptor.
  - **LBP Description:** Calculates a uniform LBP histogram to capture image texture.
  - **Combined Descriptor:** Merges HSV and LBP descriptors into a single feature vector for each image.
- **Distance Metrics:** Implements Euclidean and Chi-Squared distances to measure similarity between feature vectors.
- **Image Search Functionality:** Allows querying with an image and finds similar images based on the calculated distances.
- **Results Visualization:** Displays the most similar images to the query, along with their distances and labels.

## Installation Requirements

Ensure you have the following Python libraries installed:
- numpy
- pandas
- opencv-python (`cv2`)
- matplotlib
- scikit-image (`skimage`)
- glob

## Usage

1. Prepare your dataset and ensure the CSV file with labels is correctly formatted.
2. Run the feature extraction script to process the images and compute their descriptors.
3. Use the query functionality to search for similar images within the dataset based on a query image.
4. Visualize the results to assess the similarity of the returned images to the query.
