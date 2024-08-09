
# Music Recommendation System Using Machine Learning

This repository contains the implementation of a music recommendation system that leverages machine learning techniques to suggest songs based on user input. The system is designed to recommend music by analyzing audio features and classifying songs into different genres.

## Project Overview

The music recommendation system follows these key steps:

1. **Data Collection**: 
    - **GitHub Repository**: A collection of Hindi music spanning seven different classes: Bhajan, Bhojpuri, Bollywood Rap, Bollywood Romantic, Sufi, Garhwali, and Ghazal, with 80-100 songs per class.
    - **YouTube**: Additional music samples were collected from street artists and instrumental music, introducing two new classes: `raw_music` and `instrumentals`.

2. **Data Preprocessing**: 
    - The `librosa` library is used to extract audio features from each song, such as `onset_strength`, `MFCC`, `melspectrogram`, `chroma_cens`, and `zero_crossing_rate`.
    - These features serve as inputs to the model, with each song associated with a specific class.

3. **Models Used**:
    - **Artificial Neural Network (ANN)**:
        - A simple ANN architecture with 12 nodes in the input layer, 5 hidden layers, and 9 nodes in the output layer (one for each class).
        - Activation functions: `ReLU` and `SeLU`.
        - Optimizer: `Adam`.
        - Loss function: `cross-entropy`.
    - **K-Nearest Neighbors (KNN)**:
        - Applied after the ANN classifies the user's playlist into different genres.
        - Uses the `ball_tree` algorithm for efficient nearest neighbor search in high-dimensional spaces.

4. **Input and Output**:
    - **Input**: The user provides a playlist of song names via the terminal. The system fetches the audio files using `pytube` and `moviepy` libraries, extracts features, and predicts the genre.
    - **Output**: Based on the ANN’s classification, the system recommends songs by displaying them as strings and playing them within the Python environment.

## Results

- The system successfully trained the ANN and KNN models to recommend music based on genre classification.
- Evaluation metrics include a confusion matrix for the validation set and ROC curves for different genres.

## Conclusion

This project successfully built a music recommendation system that:
- Takes variable-sized input from users.
- Extracts audio features.
- Classifies the songs into genres using an Artificial Neural Network.
- Recommends songs based on the classification ratios.
- Plays the recommended songs within the Python environment.

## Usage

1. Clone the repository:
    ```
    git clone https://github.com/yourusername/music-recommendation-system.git
    ```

2. Install the required dependencies:
    ```
    pip install -r requirements.txt
    ```



