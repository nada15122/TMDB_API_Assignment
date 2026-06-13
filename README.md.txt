# TMDB API Testing Assignment 🎬

This repository contains the automated API testing suite for **The Movie Database (TMDB) API (v3)**, developed as part of the Route Academy Software Testing Professional Diploma.

## 📌 Project Overview
The objective of this assignment is to validate 11 different communication scenarios (Endpoints) with the TMDB API, ensuring correct status codes, data integrity, response structures, and proper authentication flow using Postman.

## 📁 Repository Contents
* **`TMDB.postman_collection.json`**: Contains all 11 API requests with comprehensive JavaScript assertions (Test Scripts).
* **`Tmdbenv.postman_environment.json`**: Contains the environment variables needed to run the collection dynamically.

## 🛠️ Environment Variables Used
The collection relies on the following variables setup in the environment file:
* `base_url`: `https://api.themoviedb.org/3`
* `api_key` & `bearer_token`: Your personal TMDB credentials for authentication.
* Dynamic IDs: `movie_id`, `series_id`, `genre_id`, `person_id`, `account_id`.

## 🚀 How to Run the Tests

### Option 1: Via Postman GUI
1. Clone this repository or download the JSON files.
2. Open Postman and click **Import**, then select both the collection and environment files.
3. Select the `Tmdbenv` environment.
4. Update the **Initial Value** of `bearer_token` and `api_key` with your credentials.
5. Right-click on the `TMDB` collection and select **Run Collection**.

### Option 2: Via Newman (CLI)
To run the tests using the command line, install Newman and execute:
```bash
newman run TMDB.postman_collection.json -e Tmdbenv.postman_environment.json