# Study-Habit-Recommender
  This project is a full-stack Study Habit Recommendation System built directly inside a Jupyter Notebook. The notebook generates and runs a FastAPI backend, a Streamlit frontend, and a SQLite database. The system analyzes student study behavior and recommends personalized study habits using data analytics and machine learning.

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

### Backend (FastAPI)
* Student Login & Signup
* Add, Edit, Delete, and View Study Logs
* Admin API for fetching all logs
* ML-powered recommendation endpoint `/recommend/{student_id}`
* Uses Pandas, NumPy, and Scikit-learn (KMeans + MinMaxScaler)
* Automatic interactive API docs via Swagger UI

### Frontend (Streamlit)
* Login system with student/admin roles
* Student dashboard
* Add study logs
* Graphs and analytics:
  * Study hours vs time
  * Study hours by subject
  * Quiz score trends
* AI recommendation page
* Admin dashboard with:
  * View all logs
  * Edit/Delete logs
  * Add students

### Recommendation Engine
The recommendation logic uses:
* Subject-wise performance
* Item-based collaborative filtering
* Clustering using KMeans
* Behavior metrics such as distraction time and consistency
* Rule-based feedback generation
* Random motivational messages

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
