# Study-Habit-Recommender
  This project is a full-stack Study Habit Recommendation System built directly inside a Jupyter Notebook. The notebook generates and runs a FastAPI backend, a Streamlit frontend, and a SQLite database. The system analyzes student study behavior and recommends personalized study habits using data analytics and ** unsupervised machine learning**.

## Overview
The notebook (`Study Habit Recommender.ipynb`) automatically:
* Creates `backend.py` (FastAPI application)
* Creates `frontend.py` (Streamlit user interface)
* Connects and manages the SQLite database (`students.db`)
* Runs the backend using Uvicorn
* Runs the Streamlit app
* Provides ngrok tunneling when used in Google Colab
* Implements a machine-learning-based recommendation engine
This allows the entire system to be executed without manually building a separate backend or frontend environment.

## Features
* **User Management:** Students can sign up and log in, and an admin role can manage data.
* **Study Log:** Students can record their daily study hours, subject, distraction time, method used, and quiz score.
* **Analysis & Clustering**: The system uses K-Means clustering to identify behavior patterns.
* **Recommendation Engine:**
  * Suggests a subject to focus on (based on collaborative filtering)
  * Picks the best study method
  * Recommends tools (like YouTube or Quizlet)
  * Provides motivational advice
* **Frontend:** A Streamlit app that presents:
  * Study logs in a table
  * Visualizations (study hours over time, subject and score trends)
  * Personalized recommendations
  * Admin dashboard to edit or delete logs
* **Backend:** FastAPI server handling API endpoints for authentication, study log operations, and recommendations

### Database
Uses a local SQLite database (`students.db`) containing:
* `students` table
* `study_logs` table

## Technologies Used
* FastAPI
* Streamlit
* SQLite
* Pandas
* NumPy
* Scikit-learn
* Requests
* Matplotlib

## Purpose
The goal of this project is to help students understand their study behavior and receive personalized recommendations to improve productivity and learning outcomes. The notebook automates deployment of a complete web application, making it easy to run both backend and frontend in any environment.
