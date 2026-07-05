# Movie Recommender System - suggestme 🎬

An end-to-end Machine Learning project that recommends movies based on the content of the movies the user has previously liked. This project utilizes a **Content-Based Filtering** approach and is deployed as an interactive web application using **Streamlit** and **Heroku**.

## 📝 Project Overview

This recommender system suggests movies by analyzing their metadata (genres, keywords, cast, and crew). It vectorizes the text data using the **Bag of Words** technique and calculates the **Cosine Similarity** between vectors to find the most conceptually similar movies in a 5000+ dimensional space.

Additionally, the project integrates with the **TMDB API** to dynamically fetch and display high-quality movie posters alongside the recommendations.

## ✨ Features
* **Content-Based Filtering:** Recommends movies similar to the user's input based on tags generated from genres, cast, director, and plot overview.
* **Text Preprocessing:** Utilizes `nltk` (PorterStemmer) for word stemming to reduce feature dimensionality and improve vector accuracy.
* **Interactive UI:** A clean, minimal, and user-friendly interface built entirely in Python using Streamlit.
* **Dynamic Posters:** Fetches real-time movie posters using the TMDB API.
* **Cloud Deployment:** Configured for seamless deployment on Heroku using `Procfile` and `setup.sh`.

## 🗂️ Project Structure

* `movie_recommender_system (1).ipynb`: The core Jupyter Notebook containing data extraction, EDA, text preprocessing (handling missing values, formatting JSON objects, stemming), vectorization, and the cosine similarity matrix generation.
* `app.py`: The main Streamlit web application script that handles the user interface and API calls.
* `main.py`: Supporting Python execution script.
* `movie_dict.pkl`: A serialized Python dictionary containing the processed movie dataset required by the Streamlit app.
* `requirements.txt`: Contains all the necessary Python libraries and dependencies required to run the project.
* `Procfile`: Configuration file telling Heroku what commands to run to start the web dyno.
* `setup.sh`: Shell script used by Heroku to configure the Streamlit environment parameters (port, CORS, etc.).
* `.gitignore`: Specifies intentionally untracked files that Git should ignore.
* `Heroku Deployment.png`, `ans1.jpg`, `ans2.jpg`: Project screenshots and deployment reference images.

## 🛠️ Tech Stack & Tools
* **Programming Language:** Python 3.9+
* **Data Manipulation:** Pandas, NumPy
* **Machine Learning & NLP:** Scikit-Learn (`CountVectorizer`, `cosine_similarity`), NLTK (`PorterStemmer`)
* **Web Framework:** Streamlit
* **API Integration:** `requests` module targeting the TMDB API
* **Deployment:** Heroku

## 📊 Dataset
The model is trained on the **TMDB 5000 Movie Dataset**, which includes detailed metadata regarding movie budgets, genres, homepages, keywords, original languages, and complete cast/crew details.

## 🚀 How to Run Locally

**1. Clone the repository**
```bash
git clone [https://github.com/your-username/movie-recommender-system.git](https://github.com/your-username/movie-recommender-system.git)
cd movie-recommender-system
