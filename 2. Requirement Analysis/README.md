# 2. Requirement Analysis

## Project Name

EduGenie – Generative AI Based Personalized Learning Assistant

## Functional Requirements

The system should provide the following functionalities:

### 1. Question Answering

The system should allow students to enter a question and receive an AI-generated answer.

API Endpoint:

POST /qa

### 2. Topic Explanation

The system should allow students to enter a topic and select a learning level.

API Endpoint:

POST /explain

The explanation should be generated in a structured format.

### 3. Quiz Generation

The system should generate quiz questions from educational content.

API Endpoint:

POST /quiz

### 4. Text Summarization

The system should convert longer educational content into a shorter summary.

API Endpoint:

POST /summarize

### 5. Learning Recommendations

The system should provide learning recommendations based on:

- Topic
- Learning level
- Number of weeks

API Endpoint:

POST /learn/recommendations

## User Interface Requirements

The frontend should contain:

- Task selection
- Learning level selection
- Input field
- Generate button
- Status area
- Result section
- Copy button

## Backend Requirements

The backend should:

- Receive requests from the frontend.
- Process requests through FastAPI.
- Call the appropriate learning module.
- Communicate with Google Gemini.
- Return JSON responses.
- Handle errors safely.

## AI Requirements

The application should integrate the Google Gemini API for AI-powered content generation.

Required environment variables:

GEMINI_API_KEY

GEMINI_MODEL

USE_LOCAL_EXPLAINER

## Hardware Requirements

Minimum recommended hardware:

- Intel Core i3 or equivalent processor
- 4 GB RAM
- 2 GB free storage
- Internet connection for Gemini API

Recommended hardware:

- Intel Core i5 or equivalent
- 8 GB RAM
- SSD storage
- Stable internet connection

## Software Requirements

- Windows 10/11
- Python 3.12
- Visual Studio Code
- FastAPI
- Uvicorn
- HTML
- CSS
- JavaScript
- Google Gemini API
- python-dotenv
- pytest
