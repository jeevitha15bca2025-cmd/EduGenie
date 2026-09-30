# 3. Project Design Phase

## System Architecture

EduGenie follows a modular architecture.

The overall system consists of:

Student
   ↓
Web Frontend
HTML / CSS / JavaScript
   ↓
HTTP / JSON Request
   ↓
FastAPI Backend
   ↓
Learning Modules
   ↓
Gemini Client
   ↓
Google Gemini API
   ↓
Generated Educational Content
   ↓
Student

## Frontend Design

The frontend consists of:

- templates/index.html
- static/style.css
- static/app.js

### index.html

The HTML file provides the basic structure of the application.

It contains:

- Task selection
- Learning level
- Input field
- Generate button
- Status area
- Result section
- Copy button

### style.css

The CSS file is responsible for styling the user interface.

### app.js

The JavaScript file manages frontend interaction and communication with the FastAPI backend.

## Backend Design

The main backend file is:

main.py

The FastAPI application:

- Creates API routes.
- Receives frontend requests.
- Calls the required learning module.
- Returns JSON responses.
- Handles backend errors.

## Learning Modules

The application contains separate modules for different learning activities:

- explanation_module.py
- qna.py
- quiz_module.py
- summary_module.py
- learning_path.py

## Gemini Client

The file:

gemini_client.py

is responsible for:

- Loading environment variables.
- Reading the Gemini API key.
- Reading the configured model.
- Creating the Gemini client.
- Sending prompts.
- Receiving generated responses.
- Handling temporary failures.

## Explanation Design

The explanation module accepts:

- Topic
- Learning level

The generated explanation is structured using:

1. Simple Definition
2. Why It Is Important
3. Step-by-Step Explanation
4. Simple Example
5. Real-World Example
6. Key Points to Remember

## Data Flow

Student Input
   ↓
Frontend JavaScript
   ↓
FastAPI Endpoint
   ↓
Learning Module
   ↓
Gemini Client
   ↓
Google Gemini
   ↓
Generated Response
   ↓
Frontend
   ↓
Student
