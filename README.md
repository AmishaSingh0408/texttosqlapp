 AI-Powered Text-to-SQL Assistant (Gemini + PostgreSQL)

Convert natural language questions into real PostgreSQL queries using Google's Gemini API.

This project connects:

🔹 Gemini 1.5 Flash (LLM)

🔹 PostgreSQL database

🔹 Python backend

🔹 Dynamic schema extraction

 Features

 Automatic PostgreSQL schema extraction
 Converts plain English → SQL
 Executes generated SQL safely
 Displays formatted results
 Fully interactive CLI tool

Tech Stack

Python

PostgreSQL

Gemini 1.5 Flash API

psycopg2

 Project Structure
text-to-sql/
│── main.py
│── README.md
 Setup Instructions
 Clone Repository
git clone https://github.com/yourusername/text-to-sql.git
cd text-to-sql
 Install Dependencies
pip install google-generativeai psycopg2
 Configure API & Database

Inside main.py:

GEMINI_API_KEY = "your_api_key_here"

DB_CONFIG = {
    "host": "localhost",
    "database": "postgres",
    "user": "postgres",
    "password": "your_password",
    "port": 5432
}
 Run the Project
python main.py
 How It Works

Extracts database schema dynamically

Sends schema + user question to Gemini

Gemini generates PostgreSQL query

Query is executed

Results are printed

 Example

Input:

Show top 5 customers by revenue

Generated SQL:

SELECT customer_name, SUM(amount) 
FROM orders 
GROUP BY customer_name 
ORDER BY SUM(amount) DESC 
LIMIT 5;
 Future Improvements

Add query validation layer

Add Streamlit UI

Add SQL injection guardrails

Add logging system

Deploy as Web App

 Author

Amisha Singh
Aspiring AI/ML Engineer & SDE
