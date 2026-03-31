# TMDB API Automation Framework 🚀

A comprehensive automated testing suite for The Movie Database (TMDB) API, built to demonstrate professional SQA methodologies, including API chaining, security validation, and automated reporting.

## 🛠️ Tech Stack
* **Testing Tool:** Postman
* **Execution Engine:** Newman (CLI)
* **Scripting:** JavaScript (Postman Sandbox)
* **Reporting:** Newman HTML-Extra
* **Environment:** Postman Global & Environment Variables

## 📋 Test Scenarios
The suite is organized into logical folders to mimic a real-world production pipeline:

1. **🔐 Auth & Smoke Tests:** Validates API connectivity and Bearer Token authorization.
2. **📉 Regression Suite:** End-to-End "User Journey" including:
   - Dynamic Searching (Interstellar)
   - **API Chaining:** Capturing `movie_id` from search to use in subsequent requests.
   - CRUD Operations (Add, Update, and Delete Movie Ratings).
3. **❌ Negative Testing:** Validates system resilience against:
   - Unauthorized access (401)
   - Resource not found (404)
   - Invalid input data (400)
4. **📜 Schema Validation:** Uses Ajv library to ensure the API "Contract" (data types and required fields) remains intact.

## 🚀 How to Run
1. Clone this repository.
2. Install dependencies: `npm install -g newman newman-reporter-htmlextra`
3. Run the following command:
   ```bash
   newman run TMDB_Movie_Suite.json -e TMDB_Env.json -r htmlextra
   ```

   ## 📊 Automation Report
   
>![Newman Report Summary](https://github.com/thedatafae/tmdb-api-automation-framework/raw/main/reports/summary.png)

> **🔗 [View Interactive HTML Report](https://htmlpreview.github.io/?https://github.com/thedatafae/tmdb-api-automation-framework/blob/main/reports/TMDB_API_Automation_Regression_Report.html)**

> Note: All tests passed with 100% success rate, validating data integrity across 15+ assertions.

