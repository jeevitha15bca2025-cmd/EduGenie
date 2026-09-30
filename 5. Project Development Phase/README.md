# 5. Project Development Phase

## Development Overview

EduGenie was developed as a modular Generative AI web application using Python, FastAPI, HTML, CSS, JavaScript and Google Gemini API.

## Project Structure

EduGenie/

├── .env
├── .env.example
├── .gitignore
├── main.py
├── gemini_client.py
├── explanation_module.py
├── qna.py
├── quiz_module.py
├── summary_module.py
├── learning_path.py
├── requirements.txt
│
├── static/
│   ├── app.js
│   └── style.css
│
├── templates/
│   └── index.html
│
└── tests/
    └── test_api.py

## Backend Development

The backend was developed using FastAPI.

The main backend file is:

main.py

It defines the API routes and connects frontend requests with the appropriate learning modules.

## AI Integration

Google Gemini is integrated through:

gemini_client.py

The Gemini client uses environment variables for configuration.

Required variables:

GEMINI_API_KEY
GEMINI_MODEL

## Explanation Module

The explanation module is implemented in:

explanation_module.py

The main function is:

explain_topic(topic, level)

It generates structured educational explanations based on the topic and learning level.

## Question Answering

The Q&A functionality is implemented through the /qa endpoint.

It receives a student's question and generates an educational answer.

## Quiz Generation

The quiz functionality is available through:

POST /quiz

It generates quiz questions from supplied educational content.

## Summarization

The summarization functionality is available through:

POST /summarize

It converts longer educational content into a shorter summary.

## Learning Path

The learning recommendation functionality is available through:

POST /learn/recommendations

It uses:

- Topic
- Learning level
- Number of weeks

to generate learning recommendations.

## Frontend Development

The frontend contains:

templates/index.html
static/style.css
static/app.js

JavaScript reads the user input, identifies the selected task, creates the JSON request and sends it to the appropriate FastAPI endpoint.

## Running the Application

Activate the virtual environment:

.venv\Scripts\activate.bat

Install dependencies:

pip install -r requirements.txt

Run the application:

python -m uvicorn main:app --reload

Open:

http://127.0.0.1:8000

API documentation:

http://127.0.0.1:8000/docs
