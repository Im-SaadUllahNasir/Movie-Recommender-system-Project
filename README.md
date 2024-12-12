# Movie Recommender System

## Overview

This project focuses on the development of a **Movie Recommender System** that suggests personalized movie recommendations based on user preferences. The system uses machine learning algorithms to predict movies that a user is most likely to enjoy based on their past ratings, preferences, and other features such as genre, director, and actors. This can help users discover new movies they might like while improving user engagement and experience.

The recommender system employs **Collaborative Filtering**, **Content-Based Filtering**, or **Hybrid Models** to provide the recommendations. The goal is to showcase how machine learning can be used to create personalized experiences, much like the recommendation engines used by services like Netflix, Amazon Prime, and others.

This repository contains the code for training, evaluating, and testing various recommender models.

## Dataset

The dataset used in this project is typically a movie ratings dataset such as the **MovieLens** dataset, which includes movie ratings by users, along with metadata like movie title, genre, and other features.

Some common features in the dataset include:

- **User ID**
- **Movie ID**
- **Rating**
- **Movie Title**
- **Genres** (e.g., Action, Drama, Comedy)
- **Release Year**
- **User Age**
- **User Gender**
- **Movie Metadata** (e.g., director, cast)

You can download the MovieLens dataset or use a similar movie dataset. For example, we use the **MovieLens 100k** dataset in this project.

Example Dataset (Columns):

| User ID | Movie ID | Rating | Movie Title | Genre    |
|---------|----------|--------|-------------|----------|
| 1       | 1        | 5      | Toy Story   | Animation|
| 2       | 2        | 4      | Jumanji     | Action   |
| 3       | 3        | 3      | The Matrix  | Sci-Fi   |
| 4       | 4        | 5      | Inception   | Action   |

## Features

- **Data Preprocessing**: The project includes steps for data cleaning, handling missing values, encoding categorical variables, and feature engineering.
- **Recommendation Algorithms**: Machine learning algorithms such as **Collaborative Filtering** (User-User, Item-Item), **Content-Based Filtering**, and **Hybrid Models** are implemented.
- **Evaluation Metrics**: The system is evaluated based on **Accuracy**, **Precision**, **Recall**, **F1-score**, and **AUC-ROC**.
- **Model Tuning**: Hyperparameter tuning using **GridSearchCV** to optimize the model performance.
- **Personalized Recommendations**: The system generates personalized movie recommendations for each user based on their preferences.

## Installation

To run this project, you'll need Python 3.x and the required dependencies. You can set up your environment as follows:

1. **Clone the Repository**:

    ```bash
    git clone https://github.com/yourusername/movie-recommender.git
    cd movie-recommender
    ```

2. **Create a Virtual Environment** (optional but recommended):

    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3. **Install Dependencies**:

    ```bash
    pip install -r requirements.txt
    ```

This will install all necessary libraries such as `pandas`, `numpy`, `scikit-learn`, `surprise`, `matplotlib`, and `seaborn`.

## Usage

1. **Data Preprocessing**:

   You can preprocess the dataset by running:

   ```bash
   python preprocess.py
   ```

   This script will clean the data (handle missing values, encode categorical variables, etc.) and split the dataset into training and testing sets.

2. **Train the Model**:

   After preprocessing, you can train multiple recommender models by running:

   ```bash
   python train_model.py
   ```

   This will train different classification models (e.g., **Logistic Regression**, **Random Forest**, **SVM**, etc.) and evaluate their performance using metrics such as accuracy and precision.

3. **Evaluate the Model**:

   Once the model is trained, you can evaluate its performance on the test dataset using:

   ```bash
   python evaluate_model.py
   ```

   This will display various evaluation metrics like **accuracy**, **precision**, **recall**, and **F1-score**.

4. **Make Predictions**:

   You can generate movie recommendations for a new user by running:

   ```bash
   python predict.py --user_id 123
   ```

   Replace `123` with the user ID you want to get recommendations for. This will output a list of recommended movies for that user.

### Example Output

After running `train_model.py`, you might see output like:

```
Model Accuracy: 85%
Precision: 0.87
Recall: 0.82
F1-Score: 0.84
```

### Example of Movie Recommendations (for a specific user):

```
Top 5 Recommended Movies for User 123:
1. The Shawshank Redemption
2. The Dark Knight
3. Pulp Fiction
4. Fight Club
5. Forrest Gump
```

## Model Evaluation

The performance of the recommender system is evaluated using the following metrics:

- **Accuracy**: The proportion of correct predictions (i.e., recommended movies that the user actually likes).
- **Precision**: The proportion of true positive recommendations to the total recommended movies.
- **Recall**: The proportion of true positive recommendations to the total number of movies that the user likes.
- **F1-Score**: The balance between precision and recall.
- **AUC-ROC Curve**: The Receiver Operating Characteristic (ROC) curve and the Area Under the Curve (AUC) for evaluating classification performance.

## Acknowledgments

- **Pandas** and **NumPy** for data manipulation.
- **scikit-learn** for machine learning models and evaluation metrics.
- **surprise** library for implementing collaborative filtering.
- **Matplotlib** and **Seaborn** for data visualization.
- **MovieLens** dataset for movie ratings data (or any other similar dataset).

----
