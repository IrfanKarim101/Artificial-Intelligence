# Comparative Analysis of Search Algorithms and Machine Learning Models

## Project Overview
This project involves implementing and comparing two search algorithms (BFS and DFS) and two machine learning models (KNN and LSTM) to analyze the NYC Taxi dataset. The goal is to explore the effectiveness of these algorithms and models for specific tasks, such as graph traversal and fare prediction, while addressing challenges related to data preprocessing and feature engineering.

## Table of Contents
1. [Description](#description)
2. [Software/Hardware Requirements](#softwarehardware-requirements)
3. [Dataset](#dataset)
4. [Algorithms](#algorithms)
5. [Tools Used](#tools-used)
6. [Methodology](#methodology)
7. [Results](#results)
8. [Problems Encountered](#problems-encountered)
9. [How to Run](#how-to-run)
10. [References](#references)

## Description
The project evaluates:
- **BFS and DFS**: Implemented to traverse graphs efficiently and compare runtime performance across different tree sizes.
- **KNN and LSTM**: Used to predict taxi fares based on features derived from the NYC Taxi dataset, demonstrating regression techniques and sequential learning capabilities.

## Software/Hardware Requirements
### Hardware
- Minimum 8GB RAM
- Intel i5 or equivalent processor
- 10GB of free storage

### Software
- Python 3.8+
- Libraries: 
  - NumPy
  - pandas
  - scikit-learn
  - TensorFlow/Keras
  - matplotlib
- Jupyter Notebook or any Python IDE (VSCode, PyCharm, etc.)

## Dataset
The **NYC Taxi Dataset (2013)** provides trip details of taxi rides in New York City. Key fields include:
- `tpep_pickup_datetime` / `tpep_dropoff_datetime`: Timestamps of trip start and end.
- `trip_distance`: Distance traveled during the trip.
- `fare_amount`: Total fare charged for the trip.

### Preprocessing Steps
1. Removed invalid values (e.g., zero or negative distances and fares).
2. Derived additional features:
   - **trip_duration**: Calculated in minutes.
   - **hour**: Hour of day from `tpep_pickup_datetime`.
   - **day_of_week**: Day of the week from `tpep_pickup_datetime`.
3. Standardized numerical fields for input into models.

## Algorithms
### BFS and DFS
- **BFS (Breadth-First Search)**: Explores all neighbors at the current depth level before moving deeper.
- **DFS (Depth-First Search)**: Explores as far as possible along each branch before backtracking.

### KNN (K-Nearest Neighbors)
- **Purpose**: Predict taxi fare by averaging the fares of k-nearest data points in the feature space.
- **Features**: `trip_distance`, `hour`, and `day_of_week`.

### LSTM (Long Short-Term Memory)
- **Purpose**: Predict taxi fare by learning temporal dependencies in the sequential data.
- **Architecture**:
  - Two LSTM layers with 64 units each and dropout regularization.
  - Dense output layer for regression.

## Tools Used
- **Programming Language**: Python
- **Libraries**:
  - NumPy and pandas for data manipulation
  - scikit-learn for KNN and evaluation metrics
  - TensorFlow/Keras for LSTM
  - matplotlib for visualizations

## Methodology
1. **Search Algorithms**:
   - Implemented BFS iteratively using a queue.
   - Implemented DFS recursively using backtracking.
2. **Machine Learning Models**:
   - **KNN**: Trained on numerical and categorical features to predict fare.
   - **LSTM**: Reshaped data into 3D tensors to capture sequential patterns.

## Results
- **BFS and DFS**: Execution times were compared for trees of various sizes using bar charts.
- **KNN**:
  - R-squared Score: **0.864**
- **LSTM**:
  - Training loss decreased consistently over 10 epochs.

## Problems Encountered
*To be added*

## How to Run
1. Clone this repository:
   ```bash
   git clone https://github.com/IrfanKarim101/Artificial-Intelligence.git
   ```
2. Navigate to the project directory:
   ```bash
   cd Artificial-Intelligence/model-ai
   ```
3. Install the required libraries:
   ```bash
   pip install -r requirements.txt
   ```
4. Run the scripts in your preferred IDE or Jupyter Notebook.

## References
1. NYC Taxi dataset documentation.
2. scikit-learn and TensorFlow/Keras official documentation.
3. "Deep Learning" by Ian Goodfellow et al.
4. Online tutorials and resources on BFS/DFS algorithms.

## GitHub Repository
[Project Repository](https://github.com/IrfanKarim101/Artificial-Intelligence/tree/e7b59535f89c940e1ef5611dc98c5ced3f69d08e/model-ai)
